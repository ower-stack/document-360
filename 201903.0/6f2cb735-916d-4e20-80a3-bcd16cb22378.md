<!--used to be: http://spryker.github.io/tutorials/zed/create-table-view/-->

This tutorial explains how to retrieve data from the database and render it in a table.

**Prerequisites:**

* You have created a new [module](https://documentation.spryker.com/v4/docs/t-add-new-bundle).

## Create a QueryContainer
1. Create the `QueryContainer` class in the `HelloWorld` module:

```
mkdir -p src/Pyz/Zed/HelloWorld/Persistence/
touch src/Pyz/Zed/HelloWorld/Persistence/HelloWorldQueryContainer.php
```

2. Add the `queryProducts` operation in the query container:

```php
<?php
namespace Pyz\Zed\HelloWorld\Persistence;

use Orm\Zed\Product\Persistence\SpyProductQuery;
use Spryker\Zed\Kernel\Persistence\AbstractQueryContainer;

interface HelloWorldQueryContainerInterface
{
    public function queryProducts();
}
```

```php
<?php
namespace Pyz\Zed\HelloWorld\Persistence;

use Orm\Zed\Product\Persistence\SpyProductQuery;
use Spryker\Zed\Kernel\Persistence\AbstractQueryContainer;

class HelloWorldQueryContainer extends AbstractQueryContainer implements HelloWorldQueryContainerInterface
{
    public function queryProducts()
    {
        return new SpyProductQuery();
    }
}
```

## Create the Table
1. Create the `ProductTable` class:

```
mkdir -p src/Pyz/Zed/HelloWorld/Communication/Table
touch src/Pyz/Zed/HelloWorld/Communication/Table/ProductTable.php
```

2. Add the configuration for the table:

<details open>
<summary>Code sample:</summary>
    
```php
<?php
namespace Pyz\Zed\HelloWorld\Communication\Table;

use Orm\Zed\Product\Persistence\Map\SpyProductTableMap;
use Orm\Zed\Product\Persistence\SpyProductQuery;
use Pyz\Zed\HelloWorld\Persistence\HelloWorldQueryContainerInterface;
use Spryker\Zed\Gui\Communication\Table\AbstractTable;
use Spryker\Zed\Gui\Communication\Table\TableConfiguration;

class ProductTable extends AbstractTable
{

    /**
     * @var \Pyz\Zed\HelloWorld\Persistence\HelloWorldQueryContainerInterface
     */
    protected $queryContainer;

    /**
     * @param \Pyz\Zed\HelloWorld\Persistence\HelloWorldQueryContainerInterface $queryContainer
     */
    public function __construct(HelloWorldQueryContainerInterface $queryContainer)
    {
        $this->queryContainer = $queryContainer;
    }

    /**
     * @param TableConfiguration $config
     *
     * @return TableConfiguration
     */
    protected function configure(TableConfiguration $config)
    {
        $config->setHeader([
            SpyProductTableMap::COL_ID_PRODUCT => 'Product ID',
            SpyProductTableMap::COL_SKU => 'Product Sku',
            ]);

        return $config;
    }

    /**
     * @param TableConfiguration $config
     *
     * @return array
     */
    protected function prepareData(TableConfiguration $config)
    {
        $queryResult = $this->runQuery($this->queryContainer->queryProducts(), $config);

        $results = [];
        foreach ($queryResult as $resultItem)
        {
            $results[] = [
                SpyProductTableMap::COL_ID_PRODUCT => $resultItem[SpyProductTableMap::COL_ID_PRODUCT],
                SpyProductTableMap::COL_SKU => $resultItem[SpyProductTableMap::COL_SKU],
            ];
        }

        return $results;
    }
}
```

</br>
</details>

## Create the Factory
The factory should be placed in the communication layer and should contain a method that returns an instance of the `ProductTable` class.

```php
touch src/Pyz/Zed/HelloWorld/Communication/HelloWorldCommunicationFactory.php
```

Add the method that constructs the instance of the `ProductTable` class:

```php
<?php
namespace Pyz\Zed\HelloWorld\Communication;

use Pyz\Zed\HelloWorld\Communication\Table\ProductTable;
use Pyz\Zed\HelloWorld\Persistence\HelloWorldQueryContainer;
use Spryker\Zed\Kernel\Communication\AbstractCommunicationFactory;

/**
 * @method HelloWorldQueryContainer getQueryContainer()
 */
class HelloWorldCommunicationFactory extends AbstractCommunicationFactory
{
    /**
     * @return ProductTable
     */
    public function createProductTable()
    {
        return new ProductTable($this->getQueryContainer());
    }
 }
```

## Add a Controller Action That Renders the Table

<details open>
<summary>Code sample:</summary>

```php
<?php
namespace Pyz\Zed\HelloWorld\Communication\Controller;

use Pyz\Zed\HelloWorld\Communication\HelloWorldCommunicationFactory;
use Spryker\Zed\Kernel\Communication\Controller\AbstractController;

/**
 * @method HelloWorldCommunicationFactory getFactory()
 */
class IndexController extends AbstractController
{
    /**
     * @return array
     */
    public function indexAction()
    {
        $table = $this->getFactory()->createProductTable();

        return [
            'products' => $table->render()
        ];
    }

    /**
     * @return \Symfony\Component\HttpFoundation\JsonResponse
     */
    public function tableAction()
    {
        $table = $this->getFactory()->createProductTable();

        return $this->jsonResponse(
            $table->fetchData()
        );
    }
}
```

</br>
</details>

@(Warning)()(The `tableAction()` will be called by a jQuery Plugin ([Datatables](https://datatables.net/)) that renders the actual data as a table.)

## Create the Twig Template
Add the products variable to `Pyz/Zed/HelloWorld/Presentation/Index/index.twig` in order to render the table containing the list of products.

```php
{% extends '@Gui/Layout/layout.twig' %}

{% block content %}

    {% embed '@Gui/Partials/widget.twig' with { widget_title: 'Orders List' } %}

        {% block widget_content %}

            {{ products | raw }}

        {% endblock %}

    {% endembed %}

{% endblock %}
```

This is all! To see the table you created, go to http://zed.de.demoshop.local/hello-world. You will be able to see the products listed in the table.
<!--Used to be: http://spryker.github.io/tutorials/yves/communication-yves-zed/-->
Yves gets most of its data from the client-side NoSQL data stores (data such as product details, product categories, prices, etc.). There are situations in which Yves needs to communicate with Zed either to submit data (e.g.: the customer has submitted a new order or subscribed to newsletter) or to retrieve data (e.g.: order history for the customer, customer account details).

In this tutorial we’ll exemplify how you can setup the communication between Yves and Zed.

We’ll display a random salutation message that is retrieved from Zed (please follow the tutorial from the _Tutorial - Adding a New Module_ article to have the backend implementation ready).

To implement this functionality, you need to follow the steps described below:

* [Create the transfer object](https://documentation.spryker.com/v4/docs/t-transfer-data-yves-zed#create-the-transfer-object)
* [Create the Gateway Controller](https://documentation.spryker.com/v4/docs/t-transfer-data-yves-zed#create-the-gateway-controller)
* [Implement the Stub](https://documentation.spryker.com/v4/docs/t-transfer-data-yves-zed#implement-the-stub)
* [Implement the Client](https://documentation.spryker.com/v4/docs/t-transfer-data-yves-zed#implement-the-client)
* [Create the controller and view in Yves](https://documentation.spryker.com/v4/docs/t-transfer-data-yves-zed#create-controller-and-view-in-yves)

## Create the Transfer Object
@(Info)(Transfer Objects)(The communication between Yves and Zed is done using transfer objects.)

Create a new transfer object to facilitate the communication between Yves and Zed. The transfer object will be added under the `src/Pyz/Shared/HelloWorld/Transfer/` folder. We’ll call it `helloworld.transfer.xml` and it will contain one property:

```xml
<?xml version="1.0"?>
<transfers xmlns="spryker:transfer-01"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="spryker:transfer-01 http://static.spryker.com/transfer-01.xsd">

    <transfer name="HelloWorldMessage">
        <property name="value" type="string" />
    </transfer>

</transfers>
```

Now, run the console command to generate the transfer object so that it’s ready to be used:

```bash
console transfer:generate
```

Add an operation to your `HelloWorldFacade` that will return the random salutation message using the transfer object you just defined:

```php
<?php
/**
 * @return \Generated\Shared\Transfer\HelloWorldMessageTransfer
 */
public function getSalutationMessage()
{
    return $this->getFactory()->createMessageGenerator()->generateHelloMessage();
}
```

<!--More information about transfer objects and how to define them in Spryker can be read here.-->

## Create the Gateway Controller
Create the `GatewayController` in Zed under `Pyz\Zed\HelloWorld\Communication\Controller`. The `GatewayController` is dedicated for communication with Yves. It must extend the `AbstractGatewayController` class.

Add an action to this controller, that will call the functionality you have exposed through your facade:

```php
<?php
namespace Pyz\Zed\HelloWorld\Communication\Controller;

use Spryker\Zed\Kernel\Communication\Controller\AbstractGatewayController;

/**
 * @method \Pyz\Zed\HelloWorld\Business\HelloWorldFacade getFacade()
 */
class GatewayController extends AbstractGatewayController
{
    /**
     *  @return \Generated\Shared\Transfer\HelloWorldMessageTransfer
     */
    public function getSalutationMessageAction()
    {
        return $this->getFacade()
                    ->getSalutationMessage();
    }
}
```

## Implement the stub
Now let’s move to the client part, to add support to call the controller action we just added. Create a `HelloWorldStub` under `src/Pyz/Client/HelloWorld/Zed`.

This stub will enable us to submit an HTTP request to Zed.

```php
<?php

namespace Pyz\Client\HelloWorld\Zed;

use Generated\Shared\Transfer\HelloWorldMessageTransfer;
use Spryker\Client\ZedRequest\ZedRequestClientInterface;

class HelloWorldStub implements HelloWorldStubInterface
{

    /**
     * @var \Spryker\Client\ZedRequest\ZedRequestClientInterface
     */
    protected $zedRequestClient;

    /**
     * @param \Spryker\Client\ZedRequest\ZedRequestClientInterface $zedRequestClient
     */
    public function __construct(ZedRequestClientInterface $zedRequestClient)
    {
        $this->zedRequestClient = $zedRequestClient;
    }

    /**
     * @return \Generated\Shared\Transfer\HelloWorldMessageTransfer
     */
    public function getSalutationMessage()
    {
        return $this->zedRequestClient->call(
            '/hello-world/gateway/get-salutation-message',
            new HelloWorldMessageTransfer()
        );
    }

}
```

@(Info)(Request parameter)(Through the second parameter you can pass a transfer object as a request parameter to the request client call.)

Add the corresponding interface for it (`HelloWorldStubInterface`) that contains the `getSalutationMessage()` method defined.

Our stub depends on the `ZedRequestClient` what we can provide by implementing `HelloWorldDependencyProvider`.

```php
<?php

namespace Pyz\Client\HelloWorld;

use Spryker\Client\Customer\CustomerDependencyProvider as SprykerCustomerDependencyProvider;
use Spryker\Client\Kernel\Container;

class HelloWorldDependencyProvider extends SprykerCustomerDependencyProvider
{

    const CLIENT_ZED_REQUEST = 'CLIENT_ZED_REQUEST';

    /**
     * @param \Spryker\Client\Kernel\Container $container
     *
     * @return \Spryker\Client\Kernel\Container
     */
    public function provideServiceLayerDependencies(Container $container)
    {
        $container = $this->addZedRequestClient($container);

        return $container;
    }

    /**
     * @param \Spryker\Client\Kernel\Container $container
     *
     * @return \Spryker\Client\Kernel\Container
     */
    protected function addZedRequestClient(Container $container)
    {
        $container[self::CLIENT_ZED_REQUEST] = function (Container $container) {
            return $container->getLocator()->zedRequest()->client();
        };

        return $container;
    }

}
```

To be able to get an instance of the `HelloWorldStub`, create the `HelloWorldFactory`:

```php
<?php

namespace Pyz\Client\HelloWorld;

use Pyz\Client\HelloWorld\Zed\HelloWorldStub;
use Spryker\Client\Kernel\AbstractFactory;

class HelloWorldFactory extends AbstractFactory
{

    /**
     * @return \Pyz\Client\HelloWorld\Zed\HelloWorldStubInterface
     */
    public function createZedStub()
    {
        return new HelloWorldStub($this->getZedRequestClient());
    }

    /**
     * @return \Spryker\Client\ZedRequest\ZedRequestClientInterface
     */
    protected function getZedRequestClient()
    {
        return $this->getProvidedDependency(HelloWorldDependencyProvider::CLIENT_ZED_REQUEST);
    }

}
```

## Implement the Client
Now that we have the `HelloWorldStub`, we can create the client that consumes this service.

Create the `HelloWorldClient` under `src/Pyz/Client/HelloWorld` together with its corresponding interface.

```php
<?php
namespace Pyz\Client\HelloWorld;

use Spryker\Client\Kernel\AbstractClient;

/**
 * @method \Pyz\Client\HelloWorld\HelloWorldFactory getFactory()
 */
class HelloWorldClient extends AbstractClient implements HelloWorldClientInterface
{
    /**
     *
     * @return \Generated\Shared\Transfer\HelloWorldMessageTransfer
     */
    public function getSalutationMessage()
    {
        return $this->getFactory()
                    ->createZedStub()
                    ->getSalutationMessage();
    }
}
```

## Create controller and view in Yves
Now that we have everything set up, we can move to Yves and create the controller and the twig template that will render the random message. Under `src/Pyz/Yves/HelloWorld/Controller`, create the `IndexController`:

```php
<?php
namespace Pyz\Yves\HelloWorld\Controller;

use Spryker\Yves\Kernel\Controller\AbstractController;

/**
 * @method \Pyz\Client\HelloWorld\HelloWorldClientInterface getClient()
 */
class IndexController extends AbstractController
{
    /**
     * @return array
     */
    public function indexAction()
    {

        return [
            'salutationMessage' => $this->getClient()->getSalutationMessage()
        ];
    }

}
```

Under `src/Pyz/Yves/HelloWorld/Theme/default/index` create the` index.twig` file:

```php
{% extends "@application/layout/layout.twig" %}

{% block content %}
    {{ salutationMessage.value }}
{% endblock %}
```
Now, the only thing left to do is to take care of the URL routing. Add the `HelloWorldControllerProvider` under `src/Pyz/Yves/HelloWorld/Plugin/Provider`:

```php
<?php
namespace Pyz\Yves\HelloWorld\Plugin\Provider;

use Pyz\Yves\Application\Plugin\Provider\AbstractYvesControllerProvider;
use Silex\Application;

class HelloWorldControllerProvider extends AbstractYvesControllerProvider
{
    /**
     * @param \Silex\Application $app
     */
    protected function defineControllers(Application $app) {
        $this->createController('/hello', 'hello', 'HelloWorld','index');
    }

}
```
Register your controller provider under YvesBootstrap:

```php
protected function getControllerProviderStack($isSsl)
	  {
		 return [
			//...
			 new HelloWorldControllerProvider($isSsl),
		 ];
	  }
```

We are done! `http://www.de.demoshop.local/hello` will now display a random salutation message.
## Install Feature API
### Prerequisites
To start feature integration, overview and install the necessary features:

| Name | Version | Required sub-feature |
| --- | --- | --- |
| Spryker Core | 201907.0 | Glue Application Feature Integration |
| Product | 201907.0 | Products API Feature Integration |
| Content Item | 201907.0 |  |

### 1) Install the Required Modules Using Composer
Run the following command(s) to install the required modules:

```bash
composer require spryker/content-banners-rest-api:"^2.1.0" spryker/content-product-abstract-lists-rest-api:"^1.0.0" --update-with-dependencies
```

@(Warning)()(Ensure that the following modules have been installed in `vendor/spryker`:)

| Module | Expected Directory |
| --- | --- |
| `ContentBannersRestApi` | `vendor/spryker/content-banners-rest-api` |
| `ContentProductAbstractListsRestApi` | `vendor/spryker/content-product-abstract-lists-rest-api` |

### 2) Set up Transfer Objects
Run the following command to generate transfer changes:

```bash
console transfer:generate
```

@(Warning)()(Make sure that the following changes have been applied in transfer objects, see    `src/Generated/Shared/Transfer/` folder:)

| Transfer | Type | Event |
| --- | --- | --- |
| `RestErrorMessage` | class | created |
| `RestContentBannerAttributes` | class | created |
| `ContentProductAbstractListType` | class | created |
| `ContentBannerType` | class | created |
| `AbstractProductsRestAttributes` | class | created |

### 3) Set up Behavior
#### Enable resources and relationships

@(Info)()(`ContentBannerResourceRoutePlugin` GET, `ContentProductAbstractListRoutePlugin` GET verbs are protected resources. Please refer to the Configure section of the *Configure documentation*.)

Activate the following plugins:

| Plugin | Specification | Prerequisites | Namespace |
| --- | --- | --- | --- |
| `ContentBannerResourceRoutePlugin` | Registers a `/content-banners/{CONTENT-KEY}` resource route. | None | `Spryker\Glue\ContentBannersRestApi\Plugin` |
| `ContentProductAbstractListRoutePlugin` | Registers a `/content-product-abstract-lists/{CONTENT-KEY}/content-product-abstract` resource route. | None | `Spryker\Glue\ContentProductAbstractListsRestApi\Plugin` |

<details open>
<summary>src/Pyz/Glue/GlueApplication/GlueApplicationDependencyProvider.php</summary>
    
```php
<?php
 
namespace Pyz\Glue\GlueApplication;
 
use Spryker\Glue\ContentBannersRestApi\Plugin\ContentBannerResourceRoutePlugin;
use Spryker\Glue\ContentProductAbstractListsRestApi\Plugin\ContentProductAbstractListRoutePlugin;
use Spryker\Glue\GlueApplication\GlueApplicationDependencyProvider as SprykerGlueApplicationDependencyProvider;
 
class GlueApplicationDependencyProvider extends SprykerGlueApplicationDependencyProvider
{
	/**
	* {@inheritdoc}
	*
	* @return \Spryker\Glue\GlueApplicationExtension\Dependency\Plugin\ResourceRoutePluginInterface[]
	*/
	protected function getResourceRoutePlugins(): array
	{
		return [
			new ContentBannerResourceRoutePlugin(),
			new ContentProductAbstractListRoutePlugin(),
		];
	}
}
```

</br>
</details>

@(Warning)()(Make sure that the following endpoints return the result with the all necessary data (for example):<ul><li>http://glue.mysprykershop.com/content-banners/{content_key}</li><li>http://glue.mysprykershop.com/content-product-abstract-lists/{content_key}/content-product-abstract</li></ul>)

<!-- Last review date: Aug 08, 2019 by Stanislav Matveyev, Yuliia Boiko-->
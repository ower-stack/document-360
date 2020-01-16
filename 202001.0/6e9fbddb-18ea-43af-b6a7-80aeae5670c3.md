:::(Error) ()
This migration guide is a part of the [Silex migration effort](https://documentation.spryker.com/docs/silex-replacement-201903).
:::

To upgrade the module, do the following:

1. Update the module using composer:
```bash
composer require spryker/security
```
2. Remove the usage of the old service providers, if you have them in the project:
```php
\Silex\Provider\RememberMeServiceProvider
\Silex\Provider\SecurityServiceProvider
\SprykerShop\Yves\AgentPage\Plugin\Provider\AgentPageSecurityServiceProvider
\SprykerShop\Yves\CustomerPage\Plugin\Provider\CustomerSecurityServiceProvider
\SprykerShop\Yves\ShopApplication\Plugin\Provider\YvesSecurityServiceProvider
```
3. Enable the new plugins in the corresponding files:
<details open>
<summary>Yves integration</summary>

```phph
<?php

namespace Pyz\Yves\ShopApplication;


use Spryker\Yves\Security\Plugin\Application\SecurityApplicationPlugin;
use SprykerShop\Yves\ShopApplication\ShopApplicationDependencyProvider as SprykerShopApplicationDependencyProvider;

class ShopApplicationDependencyProvider extends SprykerShopApplicationDependencyProvider
{
    /**
     * @return \Spryker\Shared\ApplicationExtension\Dependency\Plugin\ApplicationPluginInterface[]
     */
    protected function getApplicationPlugins(): array
    {
        return [
            ...
            new SecurityApplicationPlugin(),
            ...
        ];
    }
}
```
<br>
</details>

4. Add the additional plugins:

```phph
<?php

namespace Pyz\Yves\Security;

use Spryker\Yves\Security\Plugin\Security\RememberMeSecurityPlugin;
use Spryker\Yves\Security\SecurityDependencyProvider as SprykerSecurityDependencyProvider;
use SprykerShop\Yves\AgentPage\Plugin\Security\AgentPageSecurityPlugin;
use SprykerShop\Yves\CustomerPage\Plugin\Security\CustomerPageSecurityPlugin;

class SecurityDependencyProvider extends SprykerSecurityDependencyProvider
{
    /**
     * @return \Spryker\Shared\SecurityExtension\Dependency\Plugin\SecurityPluginInterface[]
     */
    protected function getSecurityPlugins(): array
    {
        return [
            new RememberMeSecurityPlugin(),
            new AgentPageSecurityPlugin(),
            new CustomerPageSecurityPlugin(),
        ];
    }
}
```

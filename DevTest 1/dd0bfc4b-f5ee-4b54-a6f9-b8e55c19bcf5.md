Glossary is responsible for managing glossary keys that hold the localized content in the database.

Latest version: **3.6.1**
Last update: **22 Mar 2019**
Type: **Core Splitted**
Group: **Functional**
[View on GitHub](https://github.com/spryker/glossary/releases/tag/3.6.1)



## API (Facades)

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|      pdateAndTouchTranslation**       |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |


## Plugins

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies:

* **PHP** >=7.1
* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **MessengerExtension** ^1.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0 || ^4.0.0
* **UtilText** ^1.1.0

## Suggested Installations:

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<details open>
<summary>Previous Versions </summary>

<details open>
<summary>3.6.0</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **PHP** >=7.1
* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **MessengerExtension** ^1.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0 || ^4.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.5.2</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **PHP** >=7.1
* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0 || ^4.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.5.1</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **PHP** >=7.1
* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0 || ^4.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.5.0</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **PHP** >=7.1
* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0 || ^4.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.4.0</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **PHP** >=7.1
* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0 || ^4.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.3.5</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **PHP** >=7.1
* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0 || ^4.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.3.4</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **PHP** >=7.1
* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0 || ^4.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.3.3</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **PHP** >=7.1
* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0 || ^4.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.3.2</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **PHP** >=7.1
* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0 || ^4.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.3.1</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **PHP** >=7.1
* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0 || ^4.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.3.0</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.2.2</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.2.1</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.2.0</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.1.9</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.1.8</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.1.7</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.1.6</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.1.5</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins.
* **Twig** If you want to use Twig with Gui.

<br>
</details>

<details open>
<summary>3.1.4</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins you need to install spryker/installer.
* **Twig** If you want to use Twig with Gui you need to install spryker/twig.

<br>
</details>

<details open>
<summary>3.1.3</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins you need to install spryker/installer.
* **Twig** If you want to use Twig with Gui you need to install spryker/twig.

<br>
</details>

<details open>
<summary>3.1.2</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins you need to install spryker/installer.
* **Twig** If you want to use Twig with Gui you need to install spryker/twig.

<br>
</details>

<details open>
<summary>3.1.1</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins you need to install spryker/installer.
* **Twig** If you want to use Twig with Gui you need to install spryker/twig.

<br>
</details>

<details open>
<summary>3.1.0</summary>



## API (Facades) 

|             Facade Method             |                       Description                        |
| :-----------------------------------: | :------------------------------------------------------: |
|             **createKey**             |                                                          |
|              **hasKey**               |                                                          |
|         **getKeyIdentifier**          |                                                          |
|             **updateKey**             |                                                          |
|             **deleteKey**             |                                                          |
|            **deleteKeys**             |     Deletes keys from database with the given idKeys     |
|         **createTranslation**         |                                                          |
| **createTranslationForCurrentLocale** |                                                          |
|     **createAndTouchTranslation**     |                                                          |
|          **hasTranslation**           |                                                          |
|          **getTranslation**           |                                                          |
|         **updateTranslation**         |                                                          |
|     **updateAndTouchTranslation**     |                                                          |
|    **saveGlossaryKeyTranslations**    |                                                          |
|          **saveTranslation**          |                                                          |
|      **saveAndTouchTranslation**      |                                                          |
|         **deleteTranslation**         |                                                          |
|    **deleteTranslationsByFkKeys**     | Deletes translations from database with the given idKeys |
|             **translate**             |                                                          |
|         **translateByKeyId**          |                                                          |
|  **touchCurrentTranslationForKeyId**  |                                                          |
|     **touchTranslationForKeyId**      |                                                          |
|          **getOrCreateKey**           |                                                          |
|              **install**              |                                                          |
|         **getKeySuggestions**         |                                                          |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins you need to install spryker/installer.
* **Twig** If you want to use Twig with Gui you need to install spryker/twig.

<br>
</details>

<details open>
<summary>3.0.2</summary>



## API (Facades) 

|             Facade Method             | Description |
| :-----------------------------------: | :---------: |
|             **createKey**             |             |
|              **hasKey**               |             |
|         **getKeyIdentifier**          |             |
|             **updateKey**             |             |
|             **deleteKey**             |             |
|         **createTranslation**         |             |
| **createTranslationForCurrentLocale** |             |
|     **createAndTouchTranslation**     |             |
|          **hasTranslation**           |             |
|          **getTranslation**           |             |
|         **updateTranslation**         |             |
|     **updateAndTouchTranslation**     |             |
|    **saveGlossaryKeyTranslations**    |             |
|          **saveTranslation**          |             |
|      **saveAndTouchTranslation**      |             |
|         **deleteTranslation**         |             |
|             **translate**             |             |
|         **translateByKeyId**          |             |
|  **touchCurrentTranslationForKeyId**  |             |
|     **touchTranslationForKeyId**      |             |
|          **getOrCreateKey**           |             |
|              **install**              |             |
|         **getKeySuggestions**         |             |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins you need to install spryker/installer.
* **Twig** If you want to use Twig with Gui you need to install spryker/twig.

<br>
</details>

<details open>
<summary>3.0.1</summary>



## API (Facades) 

|             Facade Method             | Description |
| :-----------------------------------: | :---------: |
|             **createKey**             |             |
|              **hasKey**               |             |
|         **getKeyIdentifier**          |             |
|             **updateKey**             |             |
|             **deleteKey**             |             |
|         **createTranslation**         |             |
| **createTranslationForCurrentLocale** |             |
|     **createAndTouchTranslation**     |             |
|          **hasTranslation**           |             |
|          **getTranslation**           |             |
|         **updateTranslation**         |             |
|     **updateAndTouchTranslation**     |             |
|    **saveGlossaryKeyTranslations**    |             |
|          **saveTranslation**          |             |
|      **saveAndTouchTranslation**      |             |
|         **deleteTranslation**         |             |
|             **translate**             |             |
|         **translateByKeyId**          |             |
|  **touchCurrentTranslationForKeyId**  |             |
|     **touchTranslationForKeyId**      |             |
|          **getOrCreateKey**           |             |
|              **install**              |             |
|         **getKeySuggestions**         |             |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins you need to install spryker/installer.
* **Twig** If you want to use Twig with Gui you need to install spryker/twig.

<br>
</details>

<details open>
<summary>3.0.0</summary>



## API (Facades) 

|             Facade Method             | Description |
| :-----------------------------------: | :---------: |
|             **createKey**             |             |
|              **hasKey**               |             |
|         **getKeyIdentifier**          |             |
|             **updateKey**             |             |
|             **deleteKey**             |             |
|         **createTranslation**         |             |
| **createTranslationForCurrentLocale** |             |
|     **createAndTouchTranslation**     |             |
|          **hasTranslation**           |             |
|          **getTranslation**           |             |
|         **updateTranslation**         |             |
|     **updateAndTouchTranslation**     |             |
|    **saveGlossaryKeyTranslations**    |             |
|          **saveTranslation**          |             |
|      **saveAndTouchTranslation**      |             |
|         **deleteTranslation**         |             |
|             **translate**             |             |
|         **translateByKeyId**          |             |
|  **touchCurrentTranslationForKeyId**  |             |
|     **touchTranslationForKeyId**      |             |
|          **getOrCreateKey**           |             |
|              **install**              |             |
|         **getKeySuggestions**         |             |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Gui** ^3.0.0
* **Kernel** ^3.0.0
* **KeyBuilder** ^1.0.0
* **Locale** ^3.0.0
* **Messenger** ^3.0.0
* **PropelOrm** ^1.0.0
* **Storage** ^3.0.0
* **Symfony** ^3.0.0
* **Touch** ^3.0.0
* **UtilText** ^1.1.0

## Suggested Installations: 

* **Installer** If you want to use Installer plugins you need to install spryker/installer.
* **Twig** If you want to use Twig with Gui you need to install spryker/twig.

<br>
</details>

<details open>
<summary>2.3.0</summary>



## API (Facades) 

|             Facade Method             | Description |
| :-----------------------------------: | :---------: |
|             **createKey**             |             |
|              **hasKey**               |             |
|         **getKeyIdentifier**          |             |
|             **updateKey**             |             |
|             **deleteKey**             |             |
|         **createTranslation**         |             |
| **createTranslationForCurrentLocale** |             |
|     **createAndTouchTranslation**     |             |
|          **hasTranslation**           |             |
|          **getTranslation**           |             |
|         **updateTranslation**         |             |
|     **updateAndTouchTranslation**     |             |
|    **saveGlossaryKeyTranslations**    |             |
|          **saveTranslation**          |             |
|      **saveAndTouchTranslation**      |             |
|         **deleteTranslation**         |             |
|             **translate**             |             |
|         **translateByKeyId**          |             |
|  **touchCurrentTranslationForKeyId**  |             |
|     **touchTranslationForKeyId**      |             |
|          **getOrCreateKey**           |             |
|              **install**              |             |
|         **getKeySuggestions**         |             |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Application** ^2.0.0
* **Collector** ^2.0.0 || ^3.0.0 || ^4.0.0
* **Gui** ^2.0.0
* **Installer** ^2.0.0 || ^3.0.0
* **Kernel** ^2.0.0
* **Locale** ^2.0.0
* **Messenger** ^2.0.0
* **Propel** ^2.0.0
* **Storage** ^2.0.0
* **Symfony** ^2.0.0
* **Twig** ^2.2.0
* **Touch** ^2.0.0
* **Url** ^2.0.0

<br>
</details>

<details open>
<summary>2.2.2</summary>



## API (Facades) 

|             Facade Method             | Description |
| :-----------------------------------: | :---------: |
|             **createKey**             |             |
|              **hasKey**               |             |
|         **getKeyIdentifier**          |             |
|             **updateKey**             |             |
|             **deleteKey**             |             |
|         **createTranslation**         |             |
| **createTranslationForCurrentLocale** |             |
|     **createAndTouchTranslation**     |             |
|          **hasTranslation**           |             |
|          **getTranslation**           |             |
|         **updateTranslation**         |             |
|     **updateAndTouchTranslation**     |             |
|    **saveGlossaryKeyTranslations**    |             |
|          **saveTranslation**          |             |
|      **saveAndTouchTranslation**      |             |
|         **deleteTranslation**         |             |
|             **translate**             |             |
|         **translateByKeyId**          |             |
|  **touchCurrentTranslationForKeyId**  |             |
|     **touchTranslationForKeyId**      |             |
|          **getOrCreateKey**           |             |
|              **install**              |             |
|         **getKeySuggestions**         |             |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Application** ^2.0.0
* **Collector** ^2.0.0 || ^3.0.0 || ^4.0.0
* **Gui** ^2.0.0
* **Installer** ^2.0.0 || ^3.0.0
* **Kernel** ^2.0.0
* **Locale** ^2.0.0
* **Messenger** ^2.0.0
* **Propel** ^2.0.0
* **Storage** ^2.0.0
* **Symfony** ^2.0.0
* **Touch** ^2.0.0
* **Url** ^2.0.0

<br>
</details>

<details open>
<summary>2.2.1</summary>



## API (Facades) 

|             Facade Method             | Description |
| :-----------------------------------: | :---------: |
|             **createKey**             |             |
|              **hasKey**               |             |
|         **getKeyIdentifier**          |             |
|             **updateKey**             |             |
|             **deleteKey**             |             |
|         **createTranslation**         |             |
| **createTranslationForCurrentLocale** |             |
|     **createAndTouchTranslation**     |             |
|          **hasTranslation**           |             |
|          **getTranslation**           |             |
|         **updateTranslation**         |             |
|     **updateAndTouchTranslation**     |             |
|    **saveGlossaryKeyTranslations**    |             |
|          **saveTranslation**          |             |
|      **saveAndTouchTranslation**      |             |
|         **deleteTranslation**         |             |
|             **translate**             |             |
|         **translateByKeyId**          |             |
|  **touchCurrentTranslationForKeyId**  |             |
|     **touchTranslationForKeyId**      |             |
|          **getOrCreateKey**           |             |
|              **install**              |             |
|         **getKeySuggestions**         |             |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Application** ^2.0.0
* **Collector** ^2.0.0 || ^3.0.0
* **Gui** ^2.0.0
* **Installer** ^2.0.0 || ^3.0.0
* **Kernel** ^2.0.0
* **Locale** ^2.0.0
* **Messenger** ^2.0.0
* **Propel** ^2.0.0
* **Storage** ^2.0.0
* **Symfony** ^2.0.0
* **Touch** ^2.0.0
* **Url** ^2.0.0

<br>
</details>

<details open>
<summary>2.2.0</summary>



## API (Facades) 

|             Facade Method             | Description |
| :-----------------------------------: | :---------: |
|             **createKey**             |             |
|              **hasKey**               |             |
|         **getKeyIdentifier**          |             |
|             **updateKey**             |             |
|             **deleteKey**             |             |
|         **createTranslation**         |             |
| **createTranslationForCurrentLocale** |             |
|     **createAndTouchTranslation**     |             |
|          **hasTranslation**           |             |
|          **getTranslation**           |             |
|         **updateTranslation**         |             |
|     **updateAndTouchTranslation**     |             |
|    **saveGlossaryKeyTranslations**    |             |
|          **saveTranslation**          |             |
|      **saveAndTouchTranslation**      |             |
|         **deleteTranslation**         |             |
|             **translate**             |             |
|         **translateByKeyId**          |             |
|  **touchCurrentTranslationForKeyId**  |             |
|     **touchTranslationForKeyId**      |             |
|          **getOrCreateKey**           |             |
|              **install**              |             |
|         **getKeySuggestions**         |             |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Application** ^2.0.0
* **Collector** ^2.0.0 || ^3.0.0
* **Gui** ^2.0.0
* **Installer** ^2.0.0 || ^3.0.0
* **Kernel** ^2.0.0
* **Locale** ^2.0.0
* **Messenger** ^2.0.0
* **Propel** ^2.0.0
* **Storage** ^2.0.0
* **Symfony** ^2.0.0
* **Touch** ^2.0.0
* **Url** ^2.0.0

<br>
</details>

<details open>
<summary>2.1.2</summary>



## API (Facades) 

|             Facade Method             | Description |
| :-----------------------------------: | :---------: |
|             **createKey**             |             |
|              **hasKey**               |             |
|         **getKeyIdentifier**          |             |
|             **updateKey**             |             |
|             **deleteKey**             |             |
|         **createTranslation**         |             |
| **createTranslationForCurrentLocale** |             |
|     **createAndTouchTranslation**     |             |
|          **hasTranslation**           |             |
|          **getTranslation**           |             |
|         **updateTranslation**         |             |
|     **updateAndTouchTranslation**     |             |
|    **saveGlossaryKeyTranslations**    |             |
|          **saveTranslation**          |             |
|      **saveAndTouchTranslation**      |             |
|         **deleteTranslation**         |             |
|             **translate**             |             |
|         **translateByKeyId**          |             |
|  **touchCurrentTranslationForKeyId**  |             |
|          **getOrCreateKey**           |             |
|              **install**              |             |
|         **getKeySuggestions**         |             |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Application** ^2.0.0
* **Collector** ^2.0.0 || ^3.0.0
* **Gui** ^2.0.0
* **Installer** ^2.0.0 || ^3.0.0
* **Kernel** ^2.0.0
* **Locale** ^2.0.0
* **Messenger** ^2.0.0
* **Propel** ^2.0.0
* **Storage** ^2.0.0
* **Symfony** ^2.0.0
* **Touch** ^2.0.0
* **Url** ^2.0.0

<br>
</details>

<details open>
<summary>2.1.1</summary>



## API (Facades) 

|             Facade Method             | Description |
| :-----------------------------------: | :---------: |
|             **createKey**             |             |
|              **hasKey**               |             |
|         **getKeyIdentifier**          |             |
|             **updateKey**             |             |
|             **deleteKey**             |             |
|         **createTranslation**         |             |
| **createTranslationForCurrentLocale** |             |
|     **createAndTouchTranslation**     |             |
|          **hasTranslation**           |             |
|          **getTranslation**           |             |
|         **updateTranslation**         |             |
|     **updateAndTouchTranslation**     |             |
|    **saveGlossaryKeyTranslations**    |             |
|          **saveTranslation**          |             |
|      **saveAndTouchTranslation**      |             |
|         **deleteTranslation**         |             |
|             **translate**             |             |
|         **translateByKeyId**          |             |
|  **touchCurrentTranslationForKeyId**  |             |
|          **getOrCreateKey**           |             |
|              **install**              |             |
|         **getKeySuggestions**         |             |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Application** ^2.0.0
* **Collector** ^2.0.0 || ^3.0.0
* **Gui** ^2.0.0
* **Kernel** ^2.0.0
* **Locale** ^2.0.0
* **Messenger** ^2.0.0
* **Storage** ^2.0.0
* **Touch** ^2.0.0
* **Propel** ^2.0.0
* **Symfony** ^2.0.0
* **Url** ^2.0.0
* **Installer** ^2.0.0

<br>
</details>

<details open>
<summary>2.1.0</summary>



## API (Facades) 

|             Facade Method             | Description |
| :-----------------------------------: | :---------: |
|             **createKey**             |             |
|              **hasKey**               |             |
|         **getKeyIdentifier**          |             |
|             **updateKey**             |             |
|             **deleteKey**             |             |
|         **createTranslation**         |             |
| **createTranslationForCurrentLocale** |             |
|     **createAndTouchTranslation**     |             |
|          **hasTranslation**           |             |
|          **getTranslation**           |             |
|         **updateTranslation**         |             |
|     **updateAndTouchTranslation**     |             |
|    **saveGlossaryKeyTranslations**    |             |
|          **saveTranslation**          |             |
|      **saveAndTouchTranslation**      |             |
|         **deleteTranslation**         |             |
|             **translate**             |             |
|         **translateByKeyId**          |             |
|  **touchCurrentTranslationForKeyId**  |             |
|          **getOrCreateKey**           |             |
|              **install**              |             |
|         **getKeySuggestions**         |             |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Application** ^2.0.0
* **Collector** ^2.0.0
* **Gui** ^2.0.0
* **Kernel** ^2.0.0
* **Locale** ^2.0.0
* **Messenger** ^2.0.0
* **Storage** ^2.0.0
* **Touch** ^2.0.0
* **Propel** ^2.0.0
* **Symfony** ^2.0.0
* **Url** ^2.0.0
* **Installer** ^2.0.0

<br>
</details>

<details open>
<summary>2.0.0</summary>



## API (Facades) 

|             Facade Method             | Description |
| :-----------------------------------: | :---------: |
|             **createKey**             |             |
|              **hasKey**               |             |
|         **getKeyIdentifier**          |             |
|             **updateKey**             |             |
|             **deleteKey**             |             |
|         **createTranslation**         |             |
| **createTranslationForCurrentLocale** |             |
|     **createAndTouchTranslation**     |             |
|          **hasTranslation**           |             |
|          **getTranslation**           |             |
|         **updateTranslation**         |             |
|     **updateAndTouchTranslation**     |             |
|    **saveGlossaryKeyTranslations**    |             |
|          **saveTranslation**          |             |
|      **saveAndTouchTranslation**      |             |
|         **deleteTranslation**         |             |
|             **translate**             |             |
|         **translateByKeyId**          |             |
|  **touchCurrentTranslationForKeyId**  |             |
|          **getOrCreateKey**           |             |
|              **install**              |             |
|         **getKeySuggestions**         |             |

## Clients 

| Client Method | Description |
| :-----------: | :---------: |
| **translate** |             |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Glossary/Dependency/Plugin/GlossaryInstallerPluginInterface.php** | **installGlossaryData** |             |

## Dependencies: 

* **Application** ^2.0.0
* **Collector** ^2.0.0
* **Gui** ^2.0.0
* **Kernel** ^2.0.0
* **Locale** ^2.0.0
* **Messenger** ^2.0.0
* **Storage** ^2.0.0
* **Touch** ^2.0.0
* **Propel** ^2.0.0
* **Symfony** ^2.0.0
* **Url** ^2.0.0
* **Installer** ^2.0.0

<br>
</details>


<br>
</details>

_13 Apr 2019_
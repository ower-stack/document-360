Checkout provides the infrastructure to handle checkout workflow for an order placement call. The checkout process creates a generic approach for step processing. Each step knows how to handle the form data, where to store data is and which conditions are required in order to be able proceed to next step. StepProcess is the class that knows how to navigate through steps. Checkout contains a stack of steps provided during class creation. The instance of this class is created in CheckoutFactory and it’s used in the CheckoutController class. Each step has a corresponding controller action. Checkout extensively uses QuoteTransfer data object to populate data from customer and track the current state of the checkout.

Latest version: **4.3.0**
Last update: **19 Feb 2019**
Type: **Core Splitted**
Group: **Functional**
[View on GitHub](https://github.com/spryker/checkout/releases/tag/4.3.0)

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (rises errors)Run checkout pre-save pluginsRun checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (Oms)Run checkout post-save pluginsReturn response with boolean isSuccess and an array of errors |

## Clients

|          Client Method           |                         Description                          |
| :------------------------------: | :----------------------------------------------------------: |
|          **placeOrder**          |                      Places the order.                       |
| **isQuoteApplicableForCheckout** | Validates quote using CheckoutPreCheckPluginInterface plugins.Considers quote valid for checkout if no plugin returns with isSuccessful=false. |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   | This plugin is called after the order is placed.Set the success flag to false, if redirect should be headed to an error page afterwords |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer and 'false' is returned.Check could be passed (returns 'true') along with errors added to the checkout response.Quote transfer should not be changedDon't use this plugin to write to a DB |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutDoSaveOrderInterface.php** |                    |                                                              |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction.Fills SaveOrderTransferDoes not change Checkout Response |

## Dependencies:

* **PHP** >=7.1
* **CheckoutExtension** ^1.1.0
* **ErrorHandler** ^2.1.0
* **Kernel** ^3.0.0
* **Oms** ^5.0.0 || ^6.0.0 || ^7.0.0 || ^8.0.0
* **PermissionExtension** ^1.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0 || ^2.0.0
* **StepEngine** ^2.2.0 || ^3.2.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0


<details open>
<summary>Previous Versions </summary>

<details open>
<summary>4.2.1 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (rises errors)Run checkout pre-save pluginsRun checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (Oms)Run checkout post-save pluginsReturn response with boolean isSuccess and an array of errors |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   | This plugin is called after the order is placed.Set the success flag to false, if redirect should be headed to an error page afterwords |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer and 'false' is returned.Check could be passed (returns 'true') along with errors added to the checkout response.Quote transfer should not be changedDon't use this plugin to write to a DB |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutDoSaveOrderInterface.php** |                    |                                                              |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction.Fills SaveOrderTransferDoes not change Checkout Response |

## Dependencies:

* **PHP** >=7.1
* **CheckoutExtension** ^1.0.0
* **ErrorHandler** ^2.1.0
* **Kernel** ^3.0.0
* **Oms** ^5.0.0 || ^6.0.0 || ^7.0.0 || ^8.0.0
* **PermissionExtension** ^1.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0 || ^2.0.0
* **StepEngine** ^2.2.0 || ^3.2.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>4.2.0 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (rises errors)Run checkout pre-save pluginsRun checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (Oms)Run checkout post-save pluginsReturn response with boolean isSuccess and an array of errors |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   | This plugin is called after the order is placed.Set the success flag to false, if redirect should be headed to an error page afterwords |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer and 'false' is returned.Check could be passed (returns 'true') along with errors added to the checkout response.Quote transfer should not be changedDon't use this plugin to write to a DB |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutDoSaveOrderInterface.php** |                    |                                                              |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction.Fills SaveOrderTransferDoes not change Checkout Response |

## Dependencies:

* **PHP** >=7.1
* **CheckoutExtension** ^1.0.0
* **ErrorHandler** ^2.1.0
* **Kernel** ^3.0.0
* **Oms** ^5.0.0 || ^6.0.0 || ^7.0.0 || ^8.0.0
* **PermissionExtension** ^1.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0 || ^2.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>4.1.6 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (rises errors)Run checkout pre-save pluginsRun checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (Oms)Run checkout post-save pluginsReturn response with boolean isSuccess and an array of errors |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   | This plugin is called after the order is placed.Set the success flag to false, if redirect should be headed to an error page afterwords |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer and 'false' is returned.Check could be passed (returns 'true') along with errors added to the checkout response.Quote transfer should not be changedDon't use this plugin to write to a DB |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutDoSaveOrderInterface.php** |                    |                                                              |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction.Fills SaveOrderTransferDoes not change Checkout Response |

## Dependencies:

* **PHP** >=7.1
* **CheckoutExtension** ^1.0.0
* **ErrorHandler** ^2.1.0
* **Kernel** ^3.0.0
* **Oms** ^5.0.0 || ^6.0.0 || ^7.0.0 || ^8.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0 || ^2.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>4.1.5 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (rises errors)Run checkout pre-save pluginsRun checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (Oms)Run checkout post-save pluginsReturn response with boolean isSuccess and an array of errors |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction.Fills SaveOrderTransferDoes not change Checkout Response |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer and 'false' is returned.Check could be passed (returns 'true') along with errors added to the checkout response.Quote transfer should not be changedDon't use this plugin to write to a DB |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   | This plugin is called after the order is placed.Set the success flag to false, if redirect should be headed to an error page afterwords |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutDoSaveOrderInterface.php** |   **saveOrder**    | Retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction. |

## Dependencies:

* **PHP** >=7.1
* **ErrorHandler** ^2.1.0
* **Kernel** ^3.0.0
* **Oms** ^5.0.0 || ^6.0.0 || ^7.0.0 || ^8.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0 || ^2.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>4.1.4 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (rises errors)Run checkout pre-save pluginsRun checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (Oms)Run checkout post-save pluginsReturn response with boolean isSuccess and an array of errors |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction.Fills SaveOrderTransferDoes not change Checkout Response |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer and 'false' is returned.Check could be passed (returns 'true') along with errors added to the checkout response.Quote transfer should not be changedDon't use this plugin to write to a DB |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   | This plugin is called after the order is placed.Set the success flag to false, if redirect should be headed to an error page afterwords |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutDoSaveOrderInterface.php** |   **saveOrder**    | Retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction. |

## Dependencies:

* **PHP** >=7.1
* **ErrorHandler** ^2.1.0
* **Kernel** ^3.0.0
* **Oms** ^5.0.0 || ^6.0.0 || ^7.0.0 || ^8.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0 || ^2.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>4.1.3 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (rises errors)Run checkout pre-save pluginsRun checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (Oms)Run checkout post-save pluginsReturn response with boolean isSuccess and an array of errors |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction.Fills SaveOrderTransferDoes not change Checkout Response |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer and 'false' is returned.Check could be passed (returns 'true') along with errors added to the checkout response.Quote transfer should not be changedDon't use this plugin to write to a DB |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   | This plugin is called after the order is placed.Set the success flag to false, if redirect should be headed to an error page afterwords |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutDoSaveOrderInterface.php** |   **saveOrder**    | Retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction. |

## Dependencies:

* **PHP** >=7.1
* **ErrorHandler** ^2.1.0
* **Kernel** ^3.0.0
* **Oms** ^5.0.0 || ^6.0.0 || ^7.0.0 || ^8.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0 || ^2.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>4.1.2 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (rises errors)Run checkout pre-save pluginsRun checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (Oms)Run checkout post-save pluginsReturn response with boolean isSuccess and an array of errors |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction.Fills SaveOrderTransferDoes not change Checkout Response |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer and 'false' is returned.Check could be passed (returns 'true') along with errors added to the checkout response.Quote transfer should not be changedDon't use this plugin to write to a DB |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   | This plugin is called after the order is placed.Set the success flag to false, if redirect should be headed to an error page afterwords |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutDoSaveOrderInterface.php** |   **saveOrder**    | Retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction. |

## Dependencies:

* **PHP** >=7.1
* **ErrorHandler** ^2.1.0
* **Kernel** ^3.0.0
* **Oms** ^5.0.0 || ^6.0.0 || ^7.0.0 || ^8.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>4.1.1 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (rises errors)Run checkout pre-save pluginsRun checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (Oms)Run checkout post-save pluginsReturn response with boolean isSuccess and an array of errors |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction.Fills SaveOrderTransferDoes not change Checkout Response |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer and 'false' is returned.Check could be passed (returns 'true') along with errors added to the checkout response.Quote transfer should not be changedDon't use this plugin to write to a DB |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   | This plugin is called after the order is placed.Set the success flag to false, if redirect should be headed to an error page afterwords |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutDoSaveOrderInterface.php** |   **saveOrder**    | Retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction. |

## Dependencies:

* **PHP** >=7.1
* **ErrorHandler** ^2.1.0
* **Kernel** ^3.0.0
* **Oms** ^5.0.0 || ^6.0.0 || ^7.0.0 || ^8.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>4.1.0 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (rises errors)Run checkout pre-save pluginsRun checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (Oms)Run checkout post-save pluginsReturn response with boolean isSuccess and an array of errors |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction.Fills SaveOrderTransferDoes not change Checkout Response |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer and 'false' is returned.Check could be passed (returns 'true') along with errors added to the checkout response.Quote transfer should not be changedDon't use this plugin to write to a DB |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   | This plugin is called after the order is placed.Set the success flag to false, if redirect should be headed to an error page afterwords |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutDoSaveOrderInterface.php** |   **saveOrder**    | Retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction. |

## Dependencies:

* **PHP** >=7.1
* **ErrorHandler** ^2.1.0
* **Kernel** ^3.0.0
* **Oms** ^5.0.0 || ^6.0.0 || ^7.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>4.0.1 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (rises errors)Run checkout pre-save pluginsRun checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (Oms)Run checkout post-save pluginsReturn response with boolean isSuccess and an array of errors |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction.Fills SaveOrderTransferDoes not change Checkout Response |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer and 'false' is returned.Check could be passed (returns 'true') along with errors added to the checkout response.Quote transfer should not be changedDon't use this plugin to write to a DB |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   | This plugin is called after the order is placed.Set the success flag to false, if redirect should be headed to an error page afterwords |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutDoSaveOrderInterface.php** |   **saveOrder**    | Retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction. |

## Dependencies:

* **ErrorHandler** ^2.1.0
* **Kernel** ^3.0.0
* **Oms** ^5.0.0 || ^6.0.0 || ^7.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>4.0.0 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (rises errors)Run checkout pre-save pluginsRun checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (Oms)Run checkout post-save pluginsReturn response with boolean isSuccess and an array of errors |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction.Fills SaveOrderTransferDoes not change Checkout Response |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer and 'false' is returned.Check could be passed (returns 'true') along with errors added to the checkout response.Quote transfer should not be changedDon't use this plugin to write to a DB |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   | This plugin is called after the order is placed.Set the success flag to false, if redirect should be headed to an error page afterwords |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutDoSaveOrderInterface.php** |   **saveOrder**    | Retrieves (its) data from the quote object and saves it to the database.These plugins are already enveloped into a transaction. |

## Dependencies:

* **ErrorHandler** ^2.1.0
* **Kernel** ^3.0.0
* **Oms** ^5.0.0 || ^6.0.0 || ^7.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>3.1.1 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |

## Dependencies:

* **Kernel** ^3.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>3.1.0 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreSaveHookInterface.php** |    **preSave**     |            Do something before orderTransfer save            |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |

## Dependencies:

* **Kernel** ^3.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>3.0.1 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |

## Dependencies:

* **Kernel** ^3.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0
* **StepEngine** ^2.0.0 || ^3.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>3.0.0 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Kernel** ^3.0.0
* **PropelOrm** ^1.0.0
* **Quote** ^1.0.0
* **StepEngine** ^2.0.0
* **Symfony** ^3.0.0
* **ZedRequest** ^3.0.0
<br>
</details>

<details open>
<summary>2.2.7 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Availability** ^2.0.0 || ^3.0.0 || ^4.0.0
* **Cart** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0 || ^3.0.0
* **Kernel** ^2.0.0
* **Locale** ^2.0.0
* **Oms** ^2.0.0 || ^3.0.0 || ^4.0.0 || ^5.0.0
* **Propel** ^2.0.0
* **Sales** ^2.0.0 || ^3.0.0 || ^4.0.0
* **StepEngine** ^1.1.0
* **Stock** ^2.0.0 || ^3.0.0
* **Symfony** ^2.0.0
* **Transfer** ^2.0.0
* **ZedRequest** ^2.0.0
<br>
</details>

<details open>
<summary>2.2.6 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Availability** ^2.0.0 || ^3.0.0
* **Cart** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0 || ^3.0.0
* **Kernel** ^2.0.0
* **Locale** ^2.0.0
* **Oms** ^2.0.0 || ^3.0.0 || ^4.0.0 || ^5.0.0
* **Propel** ^2.0.0
* **Sales** ^2.0.0 || ^3.0.0
* **StepEngine** ^1.1.0
* **Stock** ^2.0.0 || ^3.0.0
* **Symfony** ^2.0.0
* **Transfer** ^2.0.0
* **ZedRequest** ^2.0.0
<br>
</details>

<details open>
<summary>2.2.5 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Availability** ^2.0.0 || ^3.0.0
* **Cart** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0 || ^3.0.0
* **Kernel** ^2.0.0
* **Locale** ^2.0.0
* **Oms** ^2.0.0 || ^3.0.0 || ^4.0.0 || ^5.0.0
* **Propel** ^2.0.0
* **Sales** ^2.0.0 || ^3.0.0
* **StepEngine** ^1.1.0
* **Stock** ^2.0.0 || ^3.0.0
* **Symfony** ^2.0.0
* **Transfer** ^2.0.0
* **ZedRequest** ^2.0.0
<br>
</details>

<details open>
<summary>2.2.4 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Availability** ^2.0.0 || ^3.0.0
* **Cart** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0
* **Kernel** ^2.0.0
* **Oms** ^2.0.0 || ^3.0.0 || ^4.0.0
* **Propel** ^2.0.0
* **Sales** ^2.0.0
* **StepEngine** ^1.1.0
* **Stock** ^2.0.0 || ^3.0.0
* **Symfony** ^2.0.0
* **Transfer** ^2.0.0
* **ZedRequest** ^2.0.0
<br>
</details>

<details open>
<summary>2.2.3 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Availability** ^2.0.0 || ^3.0.0
* **Cart** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0
* **Kernel** ^2.0.0
* **Oms** ^2.0.0 || ^3.0.0 || ^4.0.0
* **Product** ^2.0.0 || ^3.0.0
* **Propel** ^2.0.0
* **Sales** ^2.0.0
* **StepEngine** ^1.1.0
* **Stock** ^2.0.0
* **Symfony** ^2.0.0
* **Transfer** ^2.0.0
* **ZedRequest** ^2.0.0
<br>
</details>

<details open>
<summary>2.2.2 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Availability** ^2.0.0
* **Cart** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0
* **Kernel** ^2.0.0
* **Oms** ^2.0.0 || ^3.0.0 || ^4.0.0
* **Product** ^2.0.0 || ^3.0.0
* **Propel** ^2.0.0
* **Sales** ^2.0.0
* **StepEngine** ^1.1.0
* **Stock** ^2.0.0
* **Symfony** ^2.0.0
* **Transfer** ^2.0.0
* **ZedRequest** ^2.0.0
<br>
</details>

<details open>
<summary>2.2.1 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Availability** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0
* **Kernel** ^2.0.0
* **Library** ^2.0.0
* **Oms** ^2.0.0 || ^3.0.0
* **Product** ^2.0.0 || ^3.0.0
* **Propel** ^2.0.0
* **Sales** ^2.0.0
* **StepEngine** ^1.1.0
* **Stock** ^2.0.0
* **ZedRequest** ^2.0.0
<br>
</details>

<details open>
<summary>2.2.0 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Availability** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0
* **Kernel** ^2.0.0
* **Library** ^2.0.0
* **Oms** ^2.0.0 || ^3.0.0
* **Product** ^2.0.0
* **Propel** ^2.0.0
* **Sales** ^2.0.0
* **StepEngine** ^1.1.0
* **Stock** ^2.0.0
* **ZedRequest** ^2.0.0
<br>
</details>

<details open>
<summary>2.1.3 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Calculation** ^2.0.0
* **Kernel** ^2.0.0
* **Library** ^2.0.0
* **Oms** ^2.0.0 || ^3.0.0
* **ZedRequest** ^2.0.0
* **Propel** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0
* **Product** ^2.0.0
* **Sales** ^2.0.0
* **Stock** ^2.0.0
* **StepEngine** ^1.0.0
* **Availability** ^2.0.0
* **SequenceNumber** ^2.0.0
<br>
</details>

<details open>
<summary>2.1.2 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Calculation** ^2.0.0
* **Kernel** ^2.0.0
* **Library** ^2.0.0
* **Oms** ^2.0.0 || ^3.0.0
* **ZedRequest** ^2.0.0
* **Propel** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0
* **Product** ^2.0.0
* **Sales** ^2.0.0
* **Stock** ^2.0.0
* **Availability** ^2.0.0
* **SequenceNumber** ^2.0.0
<br>
</details>

<details open>
<summary>2.1.1</summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Calculation** ^2.0.0
* **Kernel** ^2.0.0
* **Library** ^2.0.0
* **Oms** \>=2.0.0 \<=3.0.0
* **ZedRequest** ^2.0.0
* **Propel** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0
* **Product** ^2.0.0
* **Sales** ^2.0.0
* **Stock** ^2.0.0
* **Availability** ^2.0.0
* **SequenceNumber** ^2.0.0
<br>
</details>

<details open>
<summary>2.1.0 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Calculation** ^2.0.0
* **Kernel** ^2.0.0
* **Library** ^2.0.0
* **Oms** ^2.0.0
* **ZedRequest** ^2.0.0
* **Propel** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0
* **Product** ^2.0.0
* **Sales** ^2.0.0
* **Stock** ^2.0.0
* **Availability** ^2.0.0
* **SequenceNumber** ^2.0.0
<br>
</details>

<details open>
<summary>2.0.0 </summary>

## API (Facades)

| Facade Method  |                         Description                          |
| :------------: | :----------------------------------------------------------: |
| **placeOrder** | Run checkout pre-condition plugins (return on error)Run checkout order saver plugins (in a transaction)Trigger state machine for all items of the new order (-> Oms)Run post-hook pluginsReturns response with boolean isSuccess |

## Clients

| Client Method  |   Description    |
| :------------: | :--------------: |
| **placeOrder** | Places the order |

## Plugins

|                            Plugin                            |       Method       |                         Description                          |
| :----------------------------------------------------------: | :----------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPreConditionInterface.php** | **checkCondition** | Checks a condition before the order is saved. If the condition fails, an error is added to the response transfer. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutSaveOrderInterface.php** |   **saveOrder**    | This plugin retrieves (its) data from the quote object and saves it to the database. |
| **/src/Spryker/Zed/Checkout/Dependency/Plugin/CheckoutPostSaveHookInterface.php** |  **executeHook**   |       This plugin is called after the order is placed.       |

## Dependencies:

* **Calculation** ^2.0.0
* **Kernel** ^2.0.0
* **Library** ^2.0.0
* **Oms** ^2.0.0
* **ZedRequest** ^2.0.0
* **Propel** ^2.0.0
* **Country** ^2.0.0
* **Customer** ^2.0.0
* **Product** ^2.0.0
* **Sales** ^2.0.0
* **Stock** ^2.0.0
* **Availability** ^2.0.0
* **SequenceNumber** ^2.0.0
<br>
</details>


<br>
</details>

_13 Apr 2019_

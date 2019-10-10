Calculation, is used to calculate quotes and totals displayed in the cart/checkout or when an order is placed. Calculation is also used to recalculate order totals after refund. The calculation module extensively uses plugins to inject calculation algorithms. You can extend the stack of calculator plugins by adding a new custom calculators (e.g. subtotal calculation).

Latest version: **4.5.1**
Last update: **09 Apr 2019**
Type: **Core Splitted**
Group: **Functional**

[View on GitHub](https://github.com/spryker/calculation/releases/tag/4.5.1)

## API (Facades)

|                     Facade Method                      |                         Description                          |
| :----------------------------------------------------: | :----------------------------------------------------------: |
|                  **recalculateQuote**                  | Maps Quote to CalculableObjectRun all calculator pluginsMaps CalculableObject to QuoteExecutes QuotePostRecalculatePluginInterface stack of plugins.Return the updated quote |
|                  **recalculateOrder**                  |      Run all calculator pluginsReturn the updated order      |
|                    **removeTotals**                    | Remove totals from QuoteTransfer to recalculate in following calculator plugins (clear state) |
|             **validateCheckoutGrandTotal**             |                                                              |
|                 **calculateItemPrice**                 | Calculates item prices, based on store tax mode (gross/net)Calculates item sum (gross/net) priceCalculate item option sum (gross/net) price |
|       **calculateProductOptionPriceAggregation**       | Calculates total item option amount uses ProductOption::getSumPrice() |
|         **calculateDiscountAmountAggregation**         | Calculates item total discount amount without additions (options, item expenses) |
|     **calculateItemDiscountAmountFullAggregation**     | Calculates item total discount amount with additions (options, item expenses) |
|       **calculateItemTaxAmountFullAggregation**        | Calculates item total tax amount with additions (options, item expenses) |
|              **calculateSumAggregation**               | Calculates item sum aggregation with item and additions (options, item expenses) |
|           **calculatePriceToPayAggregation**           | Calculate item price to pay with additions (options, item expenses) after discounts |
|                 **calculateSubtotal**                  | Calculate order subtotal, sum of "setSumAggregation" for each item. |
|               **calculateExpenseTotal**                | Calculate order expenses, sum of "sumPrice" for each order expense. |
|               **calculateDiscountTotal**               |       Calculate total discount amount for given quote        |
|                 **calculateTaxTotal**                  |            Calculate tax total sum all item taxes            |
|                **calculateRefundTotal**                |                Calculate total refund amount                 |
|             **calculateRefundableAmount**              |   Calculate refundable amount for items and order expenses   |
|                **calculateGrandTotal**                 |      Calculate grandTotal amount to pay after discounts      |
|             **calculateInitialGrandTotal**             |    Calculate initial grandTotal amount (before discounts)    |
|               **calculateCanceledTotal**               |           Calculate total already canceled amount            |
|               **calculateOrderTaxTotal**               | Calculate total tax amount for order, take into account canceled amount |
|            **removeAllCalculatedDiscounts**            | Loops over items and expenseSets empty \ArrayObject for calculated discounts |
|                **removeCanceledAmount**                |       Sets canceled amount to zero for provided items.       |
|                 **calculateNetTotal**                  |       Calculates order total before taxes, net total.        |
| **calculateDiscountAmountAggregationForGenericAmount** | Calculates discount amount for items and options, using generic discount amount field CalculateDiscountTransfer.unitAmount |

## Clients

|  Client Method  |                         Description                          |
| :-------------: | :----------------------------------------------------------: |
| **recalculate** | Makes Zed request.Recalculates the given quote.Executes QuotePostRecalculatePluginInterface stack of plugins.Returns updated quote. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculationPluginInterface.php** |                 |                                                              |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |

## Dependencies:

* **PHP** >=7.1
* **CalculationExtension** ^1.1.0
* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins.

<details open>
<summary>Previous Versions </summary>

<details open>
<summary>4.5.0 </summary>

## API (Facades)

|                     Facade Method                      |                         Description                          |
| :----------------------------------------------------: | :----------------------------------------------------------: |
|                  **recalculateQuote**                  | Maps Quote to CalculableObjectRun all calculator pluginsMaps CalculableObject to QuoteExecutes QuotePostRecalculatePluginInterface stack of plugins.Return the updated quote |
|                  **recalculateOrder**                  |      Run all calculator pluginsReturn the updated order      |
|                    **removeTotals**                    | Remove totals from QuoteTransfer to recalculate in following calculator plugins (clear state) |
|             **validateCheckoutGrandTotal**             | Checks if the calculated totals in the quote are still valid/consistent.If not valid then adds an error code and message to the response |
|                 **calculateItemPrice**                 | Calculates item prices, based on store tax mode (gross/net)Calculates item sum (gross/net) priceCalculate item option sum (gross/net) price |
|       **calculateProductOptionPriceAggregation**       | Calculates total item option amount uses ProductOption::getSumPrice() |
|         **calculateDiscountAmountAggregation**         | Calculates item total discount amount without additions (options, item expenses) |
|     **calculateItemDiscountAmountFullAggregation**     | Calculates item total discount amount with additions (options, item expenses) |
|       **calculateItemTaxAmountFullAggregation**        | Calculates item total tax amount with additions (options, item expenses) |
|              **calculateSumAggregation**               | Calculates item sum aggregation with item and additions (options, item expenses) |
|           **calculatePriceToPayAggregation**           | Calculate item price to pay with additions (options, item expenses) after discounts |
|                 **calculateSubtotal**                  | Calculate order subtotal, sum of "setSumAggregation" for each item. |
|               **calculateExpenseTotal**                | Calculate order expenses, sum of "sumPrice" for each order expense. |
|               **calculateDiscountTotal**               |       Calculate total discount amount for given quote        |
|                 **calculateTaxTotal**                  |            Calculate tax total sum all item taxes            |
|                **calculateRefundTotal**                |                Calculate total refund amount                 |
|             **calculateRefundableAmount**              |   Calculate refundable amount for items and order expenses   |
|                **calculateGrandTotal**                 |      Calculate grandTotal amount to pay after discounts      |
|             **calculateInitialGrandTotal**             |    Calculate initial grandTotal amount (before discounts)    |
|               **calculateCanceledTotal**               |           Calculate total already canceled amount            |
|               **calculateOrderTaxTotal**               | Calculate total tax amount for order, take into account canceled amount |
|            **removeAllCalculatedDiscounts**            | Loops over items and expenseSets empty \ArrayObject for calculated discounts |
|                **removeCanceledAmount**                |       Sets canceled amount to zero for provided items.       |
|                 **calculateNetTotal**                  |       Calculates order total before taxes, net total.        |
| **calculateDiscountAmountAggregationForGenericAmount** | Calculates discount amount for items and options, using generic discount amount field CalculateDiscountTransfer.unitAmount |

## Clients

|  Client Method  |                         Description                          |
| :-------------: | :----------------------------------------------------------: |
| **recalculate** | Makes Zed request.Recalculates the given quote.Executes QuotePostRecalculatePluginInterface stack of plugins.Returns updated quote. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculationPluginInterface.php** |                 |                                                              |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |

## Dependencies:

* **PHP** >=7.1
* **CalculationExtension** ^1.1.0
* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins.
<br>
</details>

<details open>
<summary>4.4.1 </summary>

## API (Facades)

|                     Facade Method                      |                         Description                          |
| :----------------------------------------------------: | :----------------------------------------------------------: |
|                  **recalculateQuote**                  | Maps Quote to CalculableObjectRun all calculator pluginsMaps CalculableObject to QuoteReturn the updated quote |
|                  **recalculateOrder**                  |      Run all calculator pluginsReturn the updated order      |
|                    **removeTotals**                    | Remove totals from QuoteTransfer to recalculate in following calculator plugins (clear state) |
|             **validateCheckoutGrandTotal**             | Checks if the calculated totals in the quote are still valid/consistent.If not valid then adds an error code and message to the response |
|                 **calculateItemPrice**                 | Calculates item prices, based on store tax mode (gross/net)Calculates item sum (gross/net) priceCalculate item option sum (gross/net) price |
|       **calculateProductOptionPriceAggregation**       | Calculates total item option amount uses ProductOption::getSumPrice() |
|         **calculateDiscountAmountAggregation**         | Calculates item total discount amount without additions (options, item expenses) |
|     **calculateItemDiscountAmountFullAggregation**     | Calculates item total discount amount with additions (options, item expenses) |
|       **calculateItemTaxAmountFullAggregation**        | Calculates item total tax amount with additions (options, item expenses) |
|              **calculateSumAggregation**               | Calculates item sum aggregation with item and additions (options, item expenses) |
|           **calculatePriceToPayAggregation**           | Calculate item price to pay with additions (options, item expenses) after discounts |
|                 **calculateSubtotal**                  | Calculate order subtotal, sum of "setSumAggregation" for each item. |
|               **calculateExpenseTotal**                | Calculate order expenses, sum of "sumPrice" for each order expense. |
|               **calculateDiscountTotal**               |       Calculate total discount amount for given quote        |
|                 **calculateTaxTotal**                  |            Calculate tax total sum all item taxes            |
|                **calculateRefundTotal**                |                Calculate total refund amount                 |
|             **calculateRefundableAmount**              |   Calculate refundable amount for items and order expenses   |
|                **calculateGrandTotal**                 |      Calculate grandTotal amount to pay after discounts      |
|             **calculateInitialGrandTotal**             |    Calculate initial grandTotal amount (before discounts)    |
|               **calculateCanceledTotal**               |           Calculate total already canceled amount            |
|               **calculateOrderTaxTotal**               | Calculate total tax amount for order, take into account canceled amount |
|            **removeAllCalculatedDiscounts**            | Loops over items and expenseSets empty \ArrayObject for calculated discounts |
|                **removeCanceledAmount**                |       Sets canceled amount to zero for provided items.       |
|                 **calculateNetTotal**                  |       Calculates order total before taxes, net total.        |
| **calculateDiscountAmountAggregationForGenericAmount** | Calculates discount amount for items and options, using generic discount amount field CalculateDiscountTransfer.unitAmount |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculationPluginInterface.php** |                 |                                                              |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |

## Dependencies:

* **PHP** >=7.1
* **CalculationExtension** ^1.0.0
* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins.
<br>
</details>

<details open>
<summary>4.4.0 </summary>

## API (Facades)

|                     Facade Method                      |                         Description                          |
| :----------------------------------------------------: | :----------------------------------------------------------: |
|                  **recalculateQuote**                  | Maps Quote to CalculableObjectRun all calculator pluginsMaps CalculableObject to QuoteReturn the updated quote |
|                  **recalculateOrder**                  |      Run all calculator pluginsReturn the updated order      |
|                    **removeTotals**                    | Remove totals from QuoteTransfer to recalculate in following calculator plugins (clear state) |
|             **validateCheckoutGrandTotal**             | Checks if the calculated totals in the quote are still valid/consistent.If not valid then adds an error code and message to the response |
|                 **calculateItemPrice**                 | Calculates item prices, based on store tax mode (gross/net)Calculates item sum (gross/net) priceCalculate item option sum (gross/net) price |
|       **calculateProductOptionPriceAggregation**       | Calculates total item option amount uses ProductOption::getSumPrice() |
|         **calculateDiscountAmountAggregation**         | Calculates item total discount amount without additions (options, item expenses) |
|     **calculateItemDiscountAmountFullAggregation**     | Calculates item total discount amount with additions (options, item expenses) |
|       **calculateItemTaxAmountFullAggregation**        | Calculates item total tax amount with additions (options, item expenses) |
|              **calculateSumAggregation**               | Calculates item sum aggregation with item and additions (options, item expenses) |
|           **calculatePriceToPayAggregation**           | Calculate item price to pay with additions (options, item expenses) after discounts |
|                 **calculateSubtotal**                  | Calculate order subtotal, sum of "setSumAggregation" for each item. |
|               **calculateExpenseTotal**                | Calculate order expenses, sum of "sumPrice" for each order expense. |
|               **calculateDiscountTotal**               |       Calculate total discount amount for given quote        |
|                 **calculateTaxTotal**                  |            Calculate tax total sum all item taxes            |
|                **calculateRefundTotal**                |                Calculate total refund amount                 |
|             **calculateRefundableAmount**              |   Calculate refundable amount for items and order expenses   |
|                **calculateGrandTotal**                 |      Calculate grandTotal amount to pay after discounts      |
|             **calculateInitialGrandTotal**             |    Calculate initial grandTotal amount (before discounts)    |
|               **calculateCanceledTotal**               |           Calculate total already canceled amount            |
|               **calculateOrderTaxTotal**               | Calculate total tax amount for order, take into account canceled amount |
|            **removeAllCalculatedDiscounts**            | Loops over items and expenseSets empty \ArrayObject for calculated discounts |
|                **removeCanceledAmount**                |       Sets canceled amount to zero for provided items.       |
|                 **calculateNetTotal**                  |       Calculates order total before taxes, net total.        |
| **calculateDiscountAmountAggregationForGenericAmount** | Calculates discount amount for items and options, using generic discount amount field CalculateDiscountTransfer.unitAmount |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculationPluginInterface.php** | **recalculate** |                                                              |

## Dependencies:

* **PHP** >=7.1
* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins.
<br>
</details>

<details open>
<summary>4.3.0</summary>

## API (Facades)

|                     Facade Method                      |                         Description                          |
| :----------------------------------------------------: | :----------------------------------------------------------: |
|                  **recalculateQuote**                  | Maps Quote to CalculableObjectRun all calculator pluginsMaps CalculableObject to QuoteReturn the updated quote |
|                  **recalculateOrder**                  |      Run all calculator pluginsReturn the updated order      |
|                    **removeTotals**                    | Remove totals from QuoteTransfer to recalculate in following calculator plugins (clear state) |
|             **validateCheckoutGrandTotal**             | Checks if the calculated totals in the quote are still valid/consistent.If not valid then adds an error code and message to the response |
|                 **calculateItemPrice**                 | Calculates item prices, based on store tax mode (gross/net)Calculates item sum (gross/net) priceCalculate item option sum (gross/net) price |
|       **calculateProductOptionPriceAggregation**       | Calculates total item option amount uses ProductOption::getSumPrice() |
|         **calculateDiscountAmountAggregation**         | Calculates item total discount amount without additions (options, item expenses) |
|     **calculateItemDiscountAmountFullAggregation**     | Calculates item total discount amount with additions (options, item expenses) |
|       **calculateItemTaxAmountFullAggregation**        | Calculates item total tax amount with additions (options, item expenses) |
|              **calculateSumAggregation**               | Calculates item sum aggregation with item and additions (options, item expenses) |
|           **calculatePriceToPayAggregation**           | Calculate item price to pay with additions (options, item expenses) after discounts |
|                 **calculateSubtotal**                  | Calculate order subtotal, sum of "setSumAggregation" for each item. |
|               **calculateExpenseTotal**                | Calculate order expenses, sum of "sumPrice" for each order expense. |
|               **calculateDiscountTotal**               |       Calculate total discount amount for given quote        |
|                 **calculateTaxTotal**                  |            Calculate tax total sum all item taxes            |
|                **calculateRefundTotal**                |                Calculate total refund amount                 |
|             **calculateRefundableAmount**              |   Calculate refundable amount for items and order expenses   |
|                **calculateGrandTotal**                 |      Calculate grandTotal amount to pay after discounts      |
|             **calculateInitialGrandTotal**             |    Calculate initial grandTotal amount (before discounts)    |
|               **calculateCanceledTotal**               |           Calculate total already canceled amount            |
|               **calculateOrderTaxTotal**               | Calculate total tax amount for order, take into account canceled amount |
|            **removeAllCalculatedDiscounts**            | Loops over items and expenseSets empty \ArrayObject for calculated discounts |
|                 **calculateNetTotal**                  |       Calculates order total before taxes, net total.        |
| **calculateDiscountAmountAggregationForGenericAmount** | Calculates discount amount for items and options, using generic discount amount field CalculateDiscountTransfer.unitAmount |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculationPluginInterface.php** | **recalculate** |                                                              |

## Dependencies:

* **PHP** >=7.1
* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins.
<br>
</details>

<details open>
<summary>4.2.3 </summary>

## API (Facades)

|                     Facade Method                      |                         Description                          |
| :----------------------------------------------------: | :----------------------------------------------------------: |
|                  **recalculateQuote**                  | Maps Quote to CalculableObjectRun all calculator pluginsMaps CalculableObject to QuoteReturn the updated quote |
|                  **recalculateOrder**                  |      Run all calculator pluginsReturn the updated order      |
|                    **removeTotals**                    | Remove totals from QuoteTransfer to recalculate in following calculator plugins (clear state) |
|             **validateCheckoutGrandTotal**             | Checks if the calculated totals in the quote are still valid/consistent.If not valid then adds an error code and message to the response |
|                 **calculateItemPrice**                 | Calculates item prices, based on store tax mode (gross/net)Calculates item sum (gross/net) priceCalculate item option sum (gross/net) price |
|       **calculateProductOptionPriceAggregation**       | Calculates total item option amount uses ProductOption::getSumPrice() |
|         **calculateDiscountAmountAggregation**         | Calculates item total discount amount without additions (options, item expenses) |
|     **calculateItemDiscountAmountFullAggregation**     | Calculates item total discount amount with additions (options, item expenses) |
|       **calculateItemTaxAmountFullAggregation**        | Calculates item total tax amount with additions (options, item expenses) |
|              **calculateSumAggregation**               | Calculates item sum aggregation with item and additions (options, item expenses) |
|           **calculatePriceToPayAggregation**           | Calculate item price to pay with additions (options, item expenses) after discounts |
|                 **calculateSubtotal**                  | Calculate order subtotal, sum of "setSumAggregation" for each item. |
|               **calculateExpenseTotal**                | Calculate order expenses, sum of "sumPrice" for each order expense. |
|               **calculateDiscountTotal**               |       Calculate total discount amount for given quote        |
|                 **calculateTaxTotal**                  |            Calculate tax total sum all item taxes            |
|                **calculateRefundTotal**                |                Calculate total refund amount                 |
|             **calculateRefundableAmount**              |   Calculate refundable amount for items and order expenses   |
|                **calculateGrandTotal**                 |      Calculate grandTotal amount to pay after discounts      |
|             **calculateInitialGrandTotal**             |    Calculate initial grandTotal amount (before discounts)    |
|               **calculateCanceledTotal**               |           Calculate total already canceled amount            |
|               **calculateOrderTaxTotal**               | Calculate total tax amount for order, take into account canceled amount |
|            **removeAllCalculatedDiscounts**            | Loops over items and expenseSets empty \ArrayObject for calculated discounts |
|                 **calculateNetTotal**                  |       Calculates order total before taxes, net total.        |
| **calculateDiscountAmountAggregationForGenericAmount** | Calculates discount amount for items and options, using generic discount amount field CalculateDiscountTransfer.unitAmount |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculationPluginInterface.php** | **recalculate** |                                                              |

## Dependencies:

* **PHP** >=7.1
* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins.
<br>
</details>

<details open>
<summary>4.2.2 </summary>

## API (Facades)

|                     Facade Method                      |                         Description                          |
| :----------------------------------------------------: | :----------------------------------------------------------: |
|                  **recalculateQuote**                  | Maps Quote to CalculableObjectRun all calculator pluginsMaps CalculableObject to QuoteReturn the updated quote |
|                  **recalculateOrder**                  |      Run all calculator pluginsReturn the updated order      |
|                    **removeTotals**                    | Remove totals from QuoteTransfer to recalculate in following calculator plugins (clear state) |
|             **validateCheckoutGrandTotal**             | Checks if the calculated totals in the quote are still valid/consistent.If not valid then adds an error code and message to the response |
|                 **calculateItemPrice**                 | Calculates item prices, based on store tax mode (gross/net)Calculates item sum (gross/net) priceCalculate item option sum (gross/net) price |
|       **calculateProductOptionPriceAggregation**       | Calculates total item option amount uses ProductOption::getSumPrice() |
|         **calculateDiscountAmountAggregation**         | Calculates item total discount amount without additions (options, item expenses) |
|     **calculateItemDiscountAmountFullAggregation**     | Calculates item total discount amount with additions (options, item expenses) |
|       **calculateItemTaxAmountFullAggregation**        | Calculates item total tax amount with additions (options, item expenses) |
|              **calculateSumAggregation**               | Calculates item sum aggregation with item and additions (options, item expenses) |
|           **calculatePriceToPayAggregation**           | Calculate item price to pay with additions (options, item expenses) after discounts |
|                 **calculateSubtotal**                  | Calculate order subtotal, sum of "setSumAggregation" for each item. |
|               **calculateExpenseTotal**                | Calculate order expenses, sum of "sumPrice" for each order expense. |
|               **calculateDiscountTotal**               |       Calculate total discount amount for given quote        |
|                 **calculateTaxTotal**                  |            Calculate tax total sum all item taxes            |
|                **calculateRefundTotal**                |                Calculate total refund amount                 |
|             **calculateRefundableAmount**              |   Calculate refundable amount for items and order expenses   |
|                **calculateGrandTotal**                 |      Calculate grandTotal amount to pay after discounts      |
|             **calculateInitialGrandTotal**             |    Calculate initial grandTotal amount (before discounts)    |
|               **calculateCanceledTotal**               |           Calculate total already canceled amount            |
|               **calculateOrderTaxTotal**               | Calculate total tax amount for order, take into account canceled amount |
|            **removeAllCalculatedDiscounts**            | Loops over items and expenseSets empty \ArrayObject for calculated discounts |
|                 **calculateNetTotal**                  |       Calculates order total before taxes, net total.        |
| **calculateDiscountAmountAggregationForGenericAmount** | Calculates discount amount for items and options, using generic discount amount field CalculateDiscountTransfer.unitAmount |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculationPluginInterface.php** | **recalculate** |                                                              |

## Dependencies:

* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins.
<br>
</details>

<details open>
<summary>4.2.1 </summary>

## API (Facades)

|                     Facade Method                      |                         Description                          |
| :----------------------------------------------------: | :----------------------------------------------------------: |
|                  **recalculateQuote**                  | Maps Quote to CalculableObjectRun all calculator pluginsMaps CalculableObject to QuoteReturn the updated quote |
|                  **recalculateOrder**                  |      Run all calculator pluginsReturn the updated order      |
|                    **removeTotals**                    | Remove totals from QuoteTransfer to recalculate in following calculator plugins (clear state) |
|             **validateCheckoutGrandTotal**             | Checks if the calculated totals in the quote are still valid/consistent.If not valid then adds an error code and message to the response |
|                 **calculateItemPrice**                 | Calculates item prices, based on store tax mode (gross/net)Calculates item sum (gross/net) priceCalculate item option sum (gross/net) price |
|       **calculateProductOptionPriceAggregation**       | Calculates total item option amount uses ProductOption::getSumPrice() |
|         **calculateDiscountAmountAggregation**         | Calculates item total discount amount without additions (options, item expenses) |
|     **calculateItemDiscountAmountFullAggregation**     | Calculates item total discount amount with additions (options, item expenses) |
|       **calculateItemTaxAmountFullAggregation**        | Calculates item total tax amount with additions (options, item expenses) |
|              **calculateSumAggregation**               | Calculates item sum aggregation with item and additions (options, item expenses) |
|           **calculatePriceToPayAggregation**           | Calculate item price to pay with additions (options, item expenses) after discounts |
|                 **calculateSubtotal**                  | Calculate order subtotal, sum of "setSumAggregation" for each item. |
|               **calculateExpenseTotal**                | Calculate order expenses, sum of "sumPrice" for each order expense. |
|               **calculateDiscountTotal**               |       Calculate total discount amount for given quote        |
|                 **calculateTaxTotal**                  |            Calculate tax total sum all item taxes            |
|                **calculateRefundTotal**                |                Calculate total refund amount                 |
|             **calculateRefundableAmount**              |   Calculate refundable amount for items and order expenses   |
|                **calculateGrandTotal**                 |      Calculate grandTotal amount to pay after discounts      |
|             **calculateInitialGrandTotal**             |    Calculate initial grandTotal amount (before discounts)    |
|               **calculateCanceledTotal**               |           Calculate total already canceled amount            |
|               **calculateOrderTaxTotal**               | Calculate total tax amount for order, take into account canceled amount |
|            **removeAllCalculatedDiscounts**            | Loops over items and expenseSets empty \ArrayObject for calculated discounts |
|                 **calculateNetTotal**                  |       Calculates order total before taxes, net total.        |
| **calculateDiscountAmountAggregationForGenericAmount** | Calculates discount amount for items and options, using generic discount amount field CalculateDiscountTransfer.unitAmount |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculationPluginInterface.php** | **recalculate** |                                                              |

## Dependencies:

* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins.
<br>
</details>

<details open>
<summary>4.2.0 </summary>

## API (Facades)

|                 Facade Method                  |                         Description                          |
| :--------------------------------------------: | :----------------------------------------------------------: |
|              **recalculateQuote**              | Maps Quote to CalculableObjectRun all calculator pluginsMaps CalculableObject to QuoteReturn the updated quote |
|              **recalculateOrder**              |      Run all calculator pluginsReturn the updated order      |
|                **removeTotals**                | Remove totals from QuoteTransfer to recalculate in following calculator plugins (clear state) |
|         **validateCheckoutGrandTotal**         | Checks if the calculated totals in the quote are still valid/consistent.If not valid then adds an error code and message to the response |
|             **calculateItemPrice**             | Calculates item prices, based on store tax mode (gross/net)Calculates item sum (gross/net) priceCalculate item option sum (gross/net) price |
|   **calculateProductOptionPriceAggregation**   | Calculates total item option amount uses ProductOption::getSumPrice() |
|     **calculateDiscountAmountAggregation**     | Calculates item total discount amount without additions (options, item expenses) |
| **calculateItemDiscountAmountFullAggregation** | Calculates item total discount amount with additions (options, item expenses) |
|   **calculateItemTaxAmountFullAggregation**    | Calculates item total tax amount with additions (options, item expenses) |
|          **calculateSumAggregation**           | Calculates item sum aggregation with item and additions (options, item expenses) |
|       **calculatePriceToPayAggregation**       | Calculate item price to pay with additions (options, item expenses) after discounts |
|             **calculateSubtotal**              | Calculate order subtotal, sum of "setSumAggregation" for each item. |
|           **calculateExpenseTotal**            | Calculate order expenses, sum of "sumPrice" for each order expense. |
|           **calculateDiscountTotal**           |       Calculate total discount amount for given quote        |
|             **calculateTaxTotal**              |            Calculate tax total sum all item taxes            |
|            **calculateRefundTotal**            |                Calculate total refund amount                 |
|         **calculateRefundableAmount**          |   Calculate refundable amount for items and order expenses   |
|            **calculateGrandTotal**             |      Calculate grandTotal amount to pay after discounts      |
|         **calculateInitialGrandTotal**         |    Calculate initial grandTotal amount (before discounts)    |
|           **calculateCanceledTotal**           |           Calculate total already canceled amount            |
|           **calculateOrderTaxTotal**           | Calculate total tax amount for order, take into account canceled amount |
|        **removeAllCalculatedDiscounts**        | Loops over items and expenseSets empty \ArrayObject for calculated discounts |
|             **calculateNetTotal**              |       Calculates order total before taxes, net total.        |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculationPluginInterface.php** | **recalculate** |                                                              |

## Dependencies:

* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins.
<br>
</details>

<details open>
<summary>4.1.1 </summary>

## API (Facades)

|                 Facade Method                  |                         Description                          |
| :--------------------------------------------: | :----------------------------------------------------------: |
|              **recalculateQuote**              | Maps Quote to CalculableObjectRun all calculator pluginsMaps CalculableObject to QuoteReturn the updated quote |
|              **recalculateOrder**              |      Run all calculator pluginsReturn the updated order      |
|                **removeTotals**                | Remove totals from QuoteTransfer to recalculate in following calculator plugins (clear state) |
|         **validateCheckoutGrandTotal**         | Checks if the calculated totals in the quote are still valid/consistent.If not valid then adds an error code and message to the response |
|             **calculateItemPrice**             | Calculates item prices, based on store tax mode (gross/net)Calculates item sum (gross/net) priceCalculate item option sum (gross/net) price |
|   **calculateProductOptionPriceAggregation**   | Calculates total item option amount uses ProductOption::getSumPrice() |
|     **calculateDiscountAmountAggregation**     | Calculates item total discount amount without additions (options, item expenses) |
| **calculateItemDiscountAmountFullAggregation** | Calculates item total discount amount with additions (options, item expenses) |
|   **calculateItemTaxAmountFullAggregation**    | Calculates item total tax amount with additions (options, item expenses) |
|          **calculateSumAggregation**           | Calculates item sum aggregation with item and additions (options, item expenses) |
|       **calculatePriceToPayAggregation**       | Calculate item price to pay with additions (options, item expenses) after discounts |
|             **calculateSubtotal**              | Calculate order subtotal, sum of "setSumAggregation" for each item. |
|           **calculateExpenseTotal**            | Calculate order expenses, sum of "sumPrice" for each order expense. |
|           **calculateDiscountTotal**           |       Calculate total discount amount for given quote        |
|             **calculateTaxTotal**              |            Calculate tax total sum all item taxes            |
|            **calculateRefundTotal**            |                Calculate total refund amount                 |
|         **calculateRefundableAmount**          |   Calculate refundable amount for items and order expenses   |
|            **calculateGrandTotal**             |      Calculate grandTotal amount to pay after discounts      |
|         **calculateInitialGrandTotal**         |    Calculate initial grandTotal amount (before discounts)    |
|           **calculateCanceledTotal**           |           Calculate total already canceled amount            |
|           **calculateOrderTaxTotal**           | Calculate total tax amount for order, take into account canceled amount |
|        **removeAllCalculatedDiscounts**        | Loops over items and expenseSets empty \ArrayObject for calculated discounts |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculationPluginInterface.php** | **recalculate** |                                                              |

## Dependencies:

* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins.
<br>
</details>

<details open>
<summary>4.1.0 </summary>

## API (Facades)

|                 Facade Method                  |                         Description                          |
| :--------------------------------------------: | :----------------------------------------------------------: |
|              **recalculateQuote**              | Maps Quote to CalculableObjectRun all calculator pluginsMaps CalculableObject to QuoteReturn the updated quote |
|              **recalculateOrder**              |      Run all calculator pluginsReturn the updated order      |
|                **removeTotals**                | Remove totals from QuoteTransfer to recalculate in following calculator plugins (clear state) |
|         **validateCheckoutGrandTotal**         | Checks if the calculated totals in the quote are still valid/consistent.If not valid then adds an error code and message to the response |
|             **calculateItemPrice**             | Calculates item prices, based on store tax mode (gross/net)Calculates item sum (gross/net) priceCalculate item option sum (gross/net) price |
|   **calculateProductOptionPriceAggregation**   | Calculates total item option amount uses ProductOption::getSumPrice() |
|     **calculateDiscountAmountAggregation**     | Calculates item total discount amount without additions (options, item expenses) |
| **calculateItemDiscountAmountFullAggregation** | Calculates item total discount amount with additions (options, item expenses) |
|   **calculateItemTaxAmountFullAggregation**    | Calculates item total tax amount with additions (options, item expenses) |
|          **calculateSumAggregation**           | Calculates item sum aggregation with item and additions (options, item expenses) |
|       **calculatePriceToPayAggregation**       | Calculate item price to pay with additions (options, item expenses) after discounts |
|             **calculateSubtotal**              | Calculate order subtotal, sum of "setSumAggregation" for each item. |
|           **calculateExpenseTotal**            | Calculate order expenses, sum of "sumPrice" for each order expense. |
|           **calculateDiscountTotal**           |       Calculate total discount amount for given quote        |
|             **calculateTaxTotal**              |            Calculate tax total sum all item taxes            |
|            **calculateRefundTotal**            |                Calculate total refund amount                 |
|         **calculateRefundableAmount**          |   Calculate refundable amount for items and order expenses   |
|            **calculateGrandTotal**             |      Calculate grandTotal amount to pay after discounts      |
|         **calculateInitialGrandTotal**         |    Calculate initial grandTotal amount (before discounts)    |
|           **calculateCanceledTotal**           |           Calculate total already canceled amount            |
|           **calculateOrderTaxTotal**           | Calculate total tax amount for order, take into account canceled amount |
|        **removeAllCalculatedDiscounts**        | Loops over items and expenseSets empty \ArrayObject for calculated discounts |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculationPluginInterface.php** | **recalculate** |                                                              |

## Dependencies:

* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins.
<br>
</details>

<details open>
<summary>4.0.0 </summary>

## API (Facades)

|                 Facade Method                  |                         Description                          |
| :--------------------------------------------: | :----------------------------------------------------------: |
|              **recalculateQuote**              | Maps Quote to CalculableObjectRun all calculator pluginsMaps CalculableObject to QuoteReturn the updated quote |
|              **recalculateOrder**              |      Run all calculator pluginsReturn the updated order      |
|                **removeTotals**                | Remove totals from QuoteTransfer to recalculate in following calculator plugins (clear state) |
|         **validateCheckoutGrandTotal**         | Checks if the calculated totals in the quote are still valid/consistent.If not valid then adds an error code and message to the response |
|             **calculateItemPrice**             | Calculates item prices, based on store tax mode (gross/net)Calculates item sum (gross/net) priceCalculate item option sum (gross/net) price |
|   **calculateProductOptionPriceAggregation**   | Calculates total item option amount uses ProductOption::getSumPrice() |
|     **calculateDiscountAmountAggregation**     | Calculates item total discount amount without additions (options, item expenses) |
| **calculateItemDiscountAmountFullAggregation** | Calculates item total discount amount with additions (options, item expenses) |
|   **calculateItemTaxAmountFullAggregation**    | Calculates item total tax amount with additions (options, item expenses) |
|          **calculateSumAggregation**           | Calculates item sum aggregation with item and additions (options, item expenses) |
|       **calculatePriceToPayAggregation**       | Calculate item price to pay with additions (options, item expenses) after discounts |
|             **calculateSubtotal**              | Calculate order subtotal, sum of "setSumAggregation" for each item. |
|           **calculateExpenseTotal**            | Calculate order expenses, sum of "sumPrice" for each order expense. |
|           **calculateDiscountTotal**           |       Calculate total discount amount for given quote        |
|             **calculateTaxTotal**              |            Calculate tax total sum all item taxes            |
|            **calculateRefundTotal**            |                Calculate total refund amount                 |
|         **calculateRefundableAmount**          |   Calculate refundable amount for items and order expenses   |
|            **calculateGrandTotal**             |      Calculate grandTotal amount to pay after discounts      |
|           **calculateCanceledTotal**           |           Calculate total already canceled amount            |
|           **calculateOrderTaxTotal**           | Calculate total tax amount for order, take into account canceled amount |
|        **removeAllCalculatedDiscounts**        | Loops over items and expenseSets empty \ArrayObject for calculated discounts |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculationPluginInterface.php** | **recalculate** |                                                              |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |

## Dependencies:

* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins you need to install spryker/checkout.
<br>
</details>

<details open>
<summary>3.0.1 </summary>

## API (Facades)

|           Facade Method            |                         Description                          |
| :--------------------------------: | :----------------------------------------------------------: |
|          **recalculate**           |          Executes all calculators in plugin stack.           |
| **calculateExpenseGrossSumAmount** |                          calculator                          |
|     **calculateExpenseTotals**     |                          calculator                          |
|   **calculateGrandTotalTotals**    |                          calculator                          |
|   **calculateItemGrossAmounts**    |                          calculator                          |
|    **calculateOptionGrossSum**     |                          calculator                          |
|          **removeTotals**          |                          calculator                          |
|    **calculateSubtotalTotals**     |                          calculator                          |
|   **validateCheckoutGrandTotal**   | Checks if the calculated totals in the quote are still valid/consistent.If not: Adds an error code and message to the response |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |

## Dependencies:

* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins you need to install spryker/checkout.
<br>
</details>

<details open>
<summary>3.0.0</summary>

## API (Facades)

|           Facade Method            |                         Description                          |
| :--------------------------------: | :----------------------------------------------------------: |
|          **recalculate**           |          Executes all calculators in plugin stack.           |
| **calculateExpenseGrossSumAmount** |                          calculator                          |
|     **calculateExpenseTotals**     |                          calculator                          |
|   **calculateGrandTotalTotals**    |                          calculator                          |
|   **calculateItemGrossAmounts**    |                          calculator                          |
|    **calculateOptionGrossSum**     |                          calculator                          |
|          **removeTotals**          |                          calculator                          |
|    **calculateSubtotalTotals**     |                          calculator                          |
|   **validateCheckoutGrandTotal**   | Checks if the calculated totals in the quote are still valid/consistent.If not: Adds an error code and message to the response |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |

## Dependencies:

* **Kernel** ^3.0.0
* **UtilText** ^1.1.0
* **ZedRequest** ^3.0.0

## Suggested Installations:

* **Checkout** If you want to use Checkout plugins you need to install spryker/checkout.
<br>
</details>

<details open>
<summary>2.2.0</summary>

## API (Facades)

|           Facade Method            |                         Description                          |
| :--------------------------------: | :----------------------------------------------------------: |
|          **recalculate**           |          Executes all calculators in plugin stack.           |
| **calculateExpenseGrossSumAmount** |                          calculator                          |
|     **calculateExpenseTotals**     |                          calculator                          |
|   **calculateGrandTotalTotals**    |                          calculator                          |
|   **calculateItemGrossAmounts**    |                          calculator                          |
|    **calculateOptionGrossSum**     |                          calculator                          |
|          **removeTotals**          |                          calculator                          |
|    **calculateSubtotalTotals**     |                          calculator                          |
|   **validateCheckoutGrandTotal**   | Checks if the calculated totals in the quote are still valid/consistent.If not: Adds an error code and message to the response |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |

## Dependencies:

* **Checkout** ^2.0.0
* **Kernel** ^2.0.0
* **Library** ^2.0.0
* **Transfer** ^2.0.0
* **ZedRequest** ^2.0.0
<br>
</details>

<details open>
<summary>2.1.0 </summary>

## API (Facades)

|           Facade Method            |                         Description                          |
| :--------------------------------: | :----------------------------------------------------------: |
|          **recalculate**           |          Executes all calculators in plugin stack.           |
| **calculateExpenseGrossSumAmount** |                          calculator                          |
|     **calculateExpenseTotals**     |                          calculator                          |
|   **calculateGrandTotalTotals**    |                          calculator                          |
|   **calculateItemGrossAmounts**    |                          calculator                          |
|    **calculateOptionGrossSum**     |                          calculator                          |
|          **removeTotals**          |                          calculator                          |
|    **calculateSubtotalTotals**     |                          calculator                          |
|   **validateCheckoutGrandTotal**   | Checks if the calculated totals in the quote are still valid/consistent.If not: Adds an error code and message to the response |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |

## Dependencies:

* **Checkout** ^2.0.0
* **Kernel** ^2.0.0
* **Library** ^2.0.0
* **Transfer** ^2.0.0
* **ZedRequest** ^2.0.0
<br>
</details>

<details open>
<summary>2.0.0 </summary>

## API (Facades)

|           Facade Method            |                         Description                          |
| :--------------------------------: | :----------------------------------------------------------: |
|          **recalculate**           |          Executes all calculators in plugin stack.           |
| **calculateExpenseGrossSumAmount** |                          calculator                          |
|     **calculateExpenseTotals**     |                          calculator                          |
|   **calculateGrandTotalTotals**    |                          calculator                          |
|   **calculateItemGrossAmounts**    |                          calculator                          |
|    **calculateOptionGrossSum**     |                          calculator                          |
|          **removeTotals**          |                          calculator                          |
|    **calculateSubtotalTotals**     |                          calculator                          |
|   **validateCheckoutGrandTotal**   | Checks if the calculated totals in the quote are still valid/consistent.If not: Adds an error code and message to the response |

## Clients

|  Client Method  |                       Description                        |
| :-------------: | :------------------------------------------------------: |
| **recalculate** | Recalculates the given quote and returns an updated one. |

## Plugins

|                            Plugin                            |     Method      |                         Description                          |
| :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Calculation/Dependency/Plugin/CalculatorPluginInterface.php** | **recalculate** | This plugin makes calculations based on the given quote. The result is added to the quote. |

## Dependencies:

* **Kernel** ^2.0.0
* **Sales** ^2.0.0
* **Transfer** ^2.0.0
* **Checkout** ^2.0.0
* **DiscountCalculationConnector** ^2.0.0
* **Library** ^2.0.0
* **ZedRequest** ^2.0.0
<br>
</details>


<br>
</details>

_13 Apr 2019_
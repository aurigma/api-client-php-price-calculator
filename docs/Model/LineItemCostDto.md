# # LineItemCostDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**price** | **float** | Calculated price. | [optional]
**discount** | **float** | Calculated discount. | [optional]
**quantity** | **int** | Quantity. | [optional]
**total_price** | **float** | Total price (multiplying the calculated price by the quantity). | [optional]
**total_discount** | **float** | Total discount (multiplying the calculated discount by the quantity). | [optional]
**total_cost** | **float** | Final cost including discount. | [optional]
**applied_price_rules** | [**\Aurigma\PriceCalculator\Model\AppliedPriceRuleDto[]**](AppliedPriceRuleDto.md) | Applied price rules. | [optional]
**applied_discount_rules** | [**\Aurigma\PriceCalculator\Model\AppliedDiscountRule[]**](AppliedDiscountRule.md) | Applied discount rules. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

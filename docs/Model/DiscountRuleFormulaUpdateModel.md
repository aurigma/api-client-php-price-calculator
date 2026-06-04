# # DiscountRuleFormulaUpdateModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique identifier. | [optional]
**expression** | [**\Aurigma\PriceCalculator\Model\DiscountRuleFormulaUpdateModelExpression**](DiscountRuleFormulaUpdateModelExpression.md) |  | [optional]
**quantity_from** | **int** | Quantity \&quot;from\&quot;. Optional.  Used for rules with Aurigma.PriceCalculator.WebApi.Enums.DiscountRuleFormulaType.QuantityRange type of formula. | [optional]
**quantity_to** | **int** | Quantity \&quot;to\&quot;. Optional.  Used for rules with Aurigma.PriceCalculator.WebApi.Enums.DiscountRuleFormulaType.QuantityRange type of formula. | [optional]
**cost_from** | **float** | Cost \&quot;from\&quot;. Optional.  Used for rules with Aurigma.PriceCalculator.WebApi.Enums.DiscountRuleFormulaType.CostRange type of formula. | [optional]
**cost_to** | **float** | Cost \&quot;to\&quot;. Optional.  Used for rules with Aurigma.PriceCalculator.WebApi.Enums.DiscountRuleFormulaType.CostRange type of formula. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

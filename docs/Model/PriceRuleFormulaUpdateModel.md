# # PriceRuleFormulaUpdateModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique identifier. | [optional]
**quantity_from** | **int** | Quantity \&quot;from\&quot;. Optional.  Used for rules with Aurigma.PriceCalculator.WebApi.Enums.PriceRuleFormulaType.QuantityRange type of formula. | [optional]
**quantity_to** | **int** | Quantity \&quot;to\&quot;. Optional.  Used for rules with Aurigma.PriceCalculator.WebApi.Enums.PriceRuleFormulaType.QuantityRange type of formula. | [optional]
**parameter_ranges** | [**\Aurigma\PriceCalculator\Model\PriceRuleParameterRangeUpdateModel[]**](PriceRuleParameterRangeUpdateModel.md) | Parameters range list.  Used for rules with Aurigma.PriceCalculator.WebApi.Enums.PriceRuleFormulaType.ParametersMatrix type of formula. | [optional]
**expression** | **string** | Expression. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # PriceRuleConditionDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique identifier. | [optional]
**type** | [**\Aurigma\PriceCalculator\Model\PriceRuleConditionType**](PriceRuleConditionType.md) | Type. | [optional]
**operator** | [**\Aurigma\PriceCalculator\Model\PriceRuleConditionOperatorType**](PriceRuleConditionOperatorType.md) | Operator. | [optional]
**operand** | **string** | String value of the operand. Optional.  Not used for Aurigma.PriceCalculator.WebApi.Enums.PriceRuleConditionOperatorType.IsEmpty and Aurigma.PriceCalculator.WebApi.Enums.PriceRuleConditionOperatorType.IsNotEmpty operators. | [optional]
**explanation** | **string** | Explanation of the condition operator.  For example: \&quot;The input value is one of &#39;1, 2, 3&#39;\&quot;. | [optional]
**name** | **string** | Name of parameter or option. Optional.  Used only for Aurigma.PriceCalculator.WebApi.Enums.PriceRuleConditionType.Option and Aurigma.PriceCalculator.WebApi.Enums.PriceRuleConditionType.CustomParameter types only. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

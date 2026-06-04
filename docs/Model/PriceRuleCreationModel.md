# # PriceRuleCreationModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** | Title. | [optional]
**is_active** | **bool** | Indicates if the rule is being used. | [optional]
**is_break** | **bool** | Indicates if the rule chain should be broken if the current rule is satisfied. | [optional]
**formula_type** | [**\Aurigma\PriceCalculator\Model\PriceRuleFormulaType**](PriceRuleFormulaType.md) | Formula type. | [optional]
**conditions** | [**\Aurigma\PriceCalculator\Model\PriceRuleConditionCreationModel[]**](PriceRuleConditionCreationModel.md) | Conditions of execution. | [optional]
**formulas** | [**\Aurigma\PriceCalculator\Model\PriceRuleFormulaCreationModel[]**](PriceRuleFormulaCreationModel.md) | Formulas of execution. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

# # DiscountRuleCreationModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** | Title. | [optional]
**is_active** | **bool** | Indicates if the discount is being used. | [optional]
**start_date** | **\DateTime** | Discount start date. | [optional]
**end_date** | **\DateTime** | Discount end date. Optional. | [optional]
**conditions** | [**\Aurigma\PriceCalculator\Model\DiscountRuleConditionCreationModel[]**](DiscountRuleConditionCreationModel.md) | Conditions of execution. | [optional]
**formula_type** | [**\Aurigma\PriceCalculator\Model\DiscountRuleFormulaType**](DiscountRuleFormulaType.md) | Formula type. | [optional]
**formulas** | [**\Aurigma\PriceCalculator\Model\DiscountRuleFormulaCreationModel[]**](DiscountRuleFormulaCreationModel.md) | Formulas of execution. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

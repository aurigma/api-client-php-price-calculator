# Aurigma\PriceCalculator\CostCalculationApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**costCalculationCalculateLineItemCost()**](CostCalculationApi.md#costCalculationCalculateLineItemCost) | **POST** /api/price-calculator/v1/cost-calculations/line-item | Calculates the cost of the line item. |
| [**costCalculationCalculateLineItemsCost()**](CostCalculationApi.md#costCalculationCalculateLineItemsCost) | **POST** /api/price-calculator/v1/cost-calculations/line-items | Calculates the cost of line items. |


## `costCalculationCalculateLineItemCost()`

```php
costCalculationCalculateLineItemCost($line_item_cost_calculation_model, $tenant_id): \Aurigma\PriceCalculator\Model\LineItemCostDto
```

Calculates the cost of the line item.

The tenant ID is required, it is obtained either from the query string or from the token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Code
$config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\PriceCalculator\Api\CostCalculationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$line_item_cost_calculation_model = new \Aurigma\PriceCalculator\Model\LineItemCostCalculationModel(); // \Aurigma\PriceCalculator\Model\LineItemCostCalculationModel | Calculation model.
$tenant_id = 56; // int | Tenant ID.

try {
    $result = $apiInstance->costCalculationCalculateLineItemCost($line_item_cost_calculation_model, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CostCalculationApi->costCalculationCalculateLineItemCost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **line_item_cost_calculation_model** | [**\Aurigma\PriceCalculator\Model\LineItemCostCalculationModel**](../Model/LineItemCostCalculationModel.md)| Calculation model. | |
| **tenant_id** | **int**| Tenant ID. | [optional] |

### Return type

[**\Aurigma\PriceCalculator\Model\LineItemCostDto**](../Model/LineItemCostDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `costCalculationCalculateLineItemsCost()`

```php
costCalculationCalculateLineItemsCost($line_item_cost_calculation_model, $tenant_id): \Aurigma\PriceCalculator\Model\LineItemCostDto[]
```

Calculates the cost of line items.

The tenant ID is required, it is obtained either from the query string or from the token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Code
$config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\PriceCalculator\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\PriceCalculator\Api\CostCalculationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$line_item_cost_calculation_model = array(new \Aurigma\PriceCalculator\Model\LineItemCostCalculationModel()); // \Aurigma\PriceCalculator\Model\LineItemCostCalculationModel[] | Calculation models.
$tenant_id = 56; // int | Tenant ID.

try {
    $result = $apiInstance->costCalculationCalculateLineItemsCost($line_item_cost_calculation_model, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CostCalculationApi->costCalculationCalculateLineItemsCost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **line_item_cost_calculation_model** | [**\Aurigma\PriceCalculator\Model\LineItemCostCalculationModel[]**](../Model/LineItemCostCalculationModel.md)| Calculation models. | |
| **tenant_id** | **int**| Tenant ID. | [optional] |

### Return type

[**\Aurigma\PriceCalculator\Model\LineItemCostDto[]**](../Model/LineItemCostDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

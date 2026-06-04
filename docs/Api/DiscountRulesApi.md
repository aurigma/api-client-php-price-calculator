# Aurigma\PriceCalculator\DiscountRulesApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**discountRulesActivateDiscountRule()**](DiscountRulesApi.md#discountRulesActivateDiscountRule) | **POST** /api/price-calculator/v1/discount-rules/{id}/activate | Activates the discount rule. |
| [**discountRulesCreateDiscountRule()**](DiscountRulesApi.md#discountRulesCreateDiscountRule) | **POST** /api/price-calculator/v1/discount-rules | Creates a new discount rule. |
| [**discountRulesDeactivateDiscountRule()**](DiscountRulesApi.md#discountRulesDeactivateDiscountRule) | **POST** /api/price-calculator/v1/discount-rules/{id}/deactivate | Deactivates the discount rule. |
| [**discountRulesDeleteDiscountRule()**](DiscountRulesApi.md#discountRulesDeleteDiscountRule) | **DELETE** /api/price-calculator/v1/discount-rules/{id} | Deletes a discount rule by ID. |
| [**discountRulesGetAllDiscountRules()**](DiscountRulesApi.md#discountRulesGetAllDiscountRules) | **GET** /api/price-calculator/v1/discount-rules | Returns a list of all discount rules sorted by creation time. |
| [**discountRulesGetAvailableOperators()**](DiscountRulesApi.md#discountRulesGetAvailableOperators) | **GET** /api/price-calculator/v1/discount-rules/conditions/available-operators | Returns available operators for discount rule conditions. |
| [**discountRulesGetDiscountRule()**](DiscountRulesApi.md#discountRulesGetDiscountRule) | **GET** /api/price-calculator/v1/discount-rules/{id} | Returns a discount rule by ID. |
| [**discountRulesGetDiscountRulesByProductId()**](DiscountRulesApi.md#discountRulesGetDiscountRulesByProductId) | **GET** /api/price-calculator/v1/discount-rules/filter-by-product/{productId} | Returns discount rules by product ID, sorted by creation time. |
| [**discountRulesUpdateDiscountRule()**](DiscountRulesApi.md#discountRulesUpdateDiscountRule) | **PUT** /api/price-calculator/v1/discount-rules/{id} | Updates a discount rule by ID. |
| [**discountRulesValidateRuleTitle()**](DiscountRulesApi.md#discountRulesValidateRuleTitle) | **POST** /api/price-calculator/v1/discount-rules/validate-rule-title | Validates the discount rule title. |


## `discountRulesActivateDiscountRule()`

```php
discountRulesActivateDiscountRule($id, $tenant_id)
```

Activates the discount rule.

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


$apiInstance = new Aurigma\PriceCalculator\Api\DiscountRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID of the discount rule.
$tenant_id = 56; // int | Tenant ID.

try {
    $apiInstance->discountRulesActivateDiscountRule($id, $tenant_id);
} catch (Exception $e) {
    echo 'Exception when calling DiscountRulesApi->discountRulesActivateDiscountRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID of the discount rule. | |
| **tenant_id** | **int**| Tenant ID. | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountRulesCreateDiscountRule()`

```php
discountRulesCreateDiscountRule($discount_rule_creation_model, $tenant_id): \Aurigma\PriceCalculator\Model\DiscountRuleDto
```

Creates a new discount rule.

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


$apiInstance = new Aurigma\PriceCalculator\Api\DiscountRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$discount_rule_creation_model = new \Aurigma\PriceCalculator\Model\DiscountRuleCreationModel(); // \Aurigma\PriceCalculator\Model\DiscountRuleCreationModel | The model to create a discount rule.
$tenant_id = 56; // int | Tenant ID.

try {
    $result = $apiInstance->discountRulesCreateDiscountRule($discount_rule_creation_model, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountRulesApi->discountRulesCreateDiscountRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **discount_rule_creation_model** | [**\Aurigma\PriceCalculator\Model\DiscountRuleCreationModel**](../Model/DiscountRuleCreationModel.md)| The model to create a discount rule. | |
| **tenant_id** | **int**| Tenant ID. | [optional] |

### Return type

[**\Aurigma\PriceCalculator\Model\DiscountRuleDto**](../Model/DiscountRuleDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountRulesDeactivateDiscountRule()`

```php
discountRulesDeactivateDiscountRule($id, $tenant_id)
```

Deactivates the discount rule.

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


$apiInstance = new Aurigma\PriceCalculator\Api\DiscountRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID of the discount rule.
$tenant_id = 56; // int | Tenant ID.

try {
    $apiInstance->discountRulesDeactivateDiscountRule($id, $tenant_id);
} catch (Exception $e) {
    echo 'Exception when calling DiscountRulesApi->discountRulesDeactivateDiscountRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID of the discount rule. | |
| **tenant_id** | **int**| Tenant ID. | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountRulesDeleteDiscountRule()`

```php
discountRulesDeleteDiscountRule($id, $tenant_id): \Aurigma\PriceCalculator\Model\DiscountRuleDto
```

Deletes a discount rule by ID.

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


$apiInstance = new Aurigma\PriceCalculator\Api\DiscountRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID of the discount rule.
$tenant_id = 56; // int | Tenant ID.

try {
    $result = $apiInstance->discountRulesDeleteDiscountRule($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountRulesApi->discountRulesDeleteDiscountRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID of the discount rule. | |
| **tenant_id** | **int**| Tenant ID. | [optional] |

### Return type

[**\Aurigma\PriceCalculator\Model\DiscountRuleDto**](../Model/DiscountRuleDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountRulesGetAllDiscountRules()`

```php
discountRulesGetAllDiscountRules($product_id, $tenant_id): \Aurigma\PriceCalculator\Model\DiscountRuleDto[]
```

Returns a list of all discount rules sorted by creation time.

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


$apiInstance = new Aurigma\PriceCalculator\Api\DiscountRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 56; // int | Product ID. Optional.
$tenant_id = 56; // int | Tenant ID.

try {
    $result = $apiInstance->discountRulesGetAllDiscountRules($product_id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountRulesApi->discountRulesGetAllDiscountRules: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **int**| Product ID. Optional. | [optional] |
| **tenant_id** | **int**| Tenant ID. | [optional] |

### Return type

[**\Aurigma\PriceCalculator\Model\DiscountRuleDto[]**](../Model/DiscountRuleDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountRulesGetAvailableOperators()`

```php
discountRulesGetAvailableOperators($tenant_id): \Aurigma\PriceCalculator\Model\DiscountRuleConditionsAvailableOperatorsDto
```

Returns available operators for discount rule conditions.

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


$apiInstance = new Aurigma\PriceCalculator\Api\DiscountRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant ID.

try {
    $result = $apiInstance->discountRulesGetAvailableOperators($tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountRulesApi->discountRulesGetAvailableOperators: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant ID. | [optional] |

### Return type

[**\Aurigma\PriceCalculator\Model\DiscountRuleConditionsAvailableOperatorsDto**](../Model/DiscountRuleConditionsAvailableOperatorsDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountRulesGetDiscountRule()`

```php
discountRulesGetDiscountRule($id, $tenant_id): \Aurigma\PriceCalculator\Model\DiscountRuleDto
```

Returns a discount rule by ID.

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


$apiInstance = new Aurigma\PriceCalculator\Api\DiscountRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Discount rule ID.
$tenant_id = 56; // int | Tenant ID.

try {
    $result = $apiInstance->discountRulesGetDiscountRule($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountRulesApi->discountRulesGetDiscountRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Discount rule ID. | |
| **tenant_id** | **int**| Tenant ID. | [optional] |

### Return type

[**\Aurigma\PriceCalculator\Model\DiscountRuleDto**](../Model/DiscountRuleDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountRulesGetDiscountRulesByProductId()`

```php
discountRulesGetDiscountRulesByProductId($product_id, $tenant_id): \Aurigma\PriceCalculator\Model\DiscountRuleDto[]
```

Returns discount rules by product ID, sorted by creation time.

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


$apiInstance = new Aurigma\PriceCalculator\Api\DiscountRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 56; // int
$tenant_id = 56; // int | Tenant ID.

try {
    $result = $apiInstance->discountRulesGetDiscountRulesByProductId($product_id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountRulesApi->discountRulesGetDiscountRulesByProductId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **int**|  | |
| **tenant_id** | **int**| Tenant ID. | [optional] |

### Return type

[**\Aurigma\PriceCalculator\Model\DiscountRuleDto[]**](../Model/DiscountRuleDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountRulesUpdateDiscountRule()`

```php
discountRulesUpdateDiscountRule($id, $discount_rule_update_model, $tenant_id): \Aurigma\PriceCalculator\Model\DiscountRuleDto
```

Updates a discount rule by ID.

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


$apiInstance = new Aurigma\PriceCalculator\Api\DiscountRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID of the discount rule.
$discount_rule_update_model = new \Aurigma\PriceCalculator\Model\DiscountRuleUpdateModel(); // \Aurigma\PriceCalculator\Model\DiscountRuleUpdateModel | The model to update a discount rule.
$tenant_id = 56; // int | Tenant ID.

try {
    $result = $apiInstance->discountRulesUpdateDiscountRule($id, $discount_rule_update_model, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountRulesApi->discountRulesUpdateDiscountRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID of the discount rule. | |
| **discount_rule_update_model** | [**\Aurigma\PriceCalculator\Model\DiscountRuleUpdateModel**](../Model/DiscountRuleUpdateModel.md)| The model to update a discount rule. | |
| **tenant_id** | **int**| Tenant ID. | [optional] |

### Return type

[**\Aurigma\PriceCalculator\Model\DiscountRuleDto**](../Model/DiscountRuleDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json-patch+json`, `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `discountRulesValidateRuleTitle()`

```php
discountRulesValidateRuleTitle($title, $id, $tenant_id): \Aurigma\PriceCalculator\Model\ValidationResultDto
```

Validates the discount rule title.

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


$apiInstance = new Aurigma\PriceCalculator\Api\DiscountRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$title = 'title_example'; // string | Discount rule title.
$id = 'id_example'; // string | Discount rule ID. Optional.
$tenant_id = 56; // int | Tenant ID.

try {
    $result = $apiInstance->discountRulesValidateRuleTitle($title, $id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DiscountRulesApi->discountRulesValidateRuleTitle: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **title** | **string**| Discount rule title. | [optional] |
| **id** | **string**| Discount rule ID. Optional. | [optional] |
| **tenant_id** | **int**| Tenant ID. | [optional] |

### Return type

[**\Aurigma\PriceCalculator\Model\ValidationResultDto**](../Model/ValidationResultDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Code](../../README.md#OAuth2Code), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

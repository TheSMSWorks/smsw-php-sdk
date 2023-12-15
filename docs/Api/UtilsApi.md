# OpenAPI\Client\UtilsApi

All URIs are relative to https://api.thesmsworks.co.uk/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**utilsErrorsErrorcodeGet()**](UtilsApi.md#utilsErrorsErrorcodeGet) | **GET** /utils/errors/{errorcode} |  |
| [**utilsTestGet()**](UtilsApi.md#utilsTestGet) | **GET** /utils/test |  |


## `utilsErrorsErrorcodeGet()`

```php
utilsErrorsErrorcodeGet($errorcode): \OpenAPI\Client\Model\ExtendedErrorModel
```



Returns a sample error object for the given error code. Useful for designing code to react to errors when they occur for real.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\UtilsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$errorcode = 'errorcode_example'; // string | The code of the error you would like returned

try {
    $result = $apiInstance->utilsErrorsErrorcodeGet($errorcode);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UtilsApi->utilsErrorsErrorcodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **errorcode** | **string**| The code of the error you would like returned | |

### Return type

[**\OpenAPI\Client\Model\ExtendedErrorModel**](../Model/ExtendedErrorModel.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `utilsTestGet()`

```php
utilsTestGet(): \OpenAPI\Client\Model\TestResponse
```



Returns the customer ID to the caller

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\UtilsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->utilsTestGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UtilsApi->utilsTestGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\TestResponse**](../Model/TestResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

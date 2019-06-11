# Swagger\Client\UtilsApi

All URIs are relative to *https://api.thesmsworks.co.uk/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getError**](UtilsApi.md#getError) | **GET** /utils/errors/{errorcode} | 
[**test**](UtilsApi.md#test) | **GET** /utils/test | 

# **getError**
> \Swagger\Client\Model\ExtendedErrorModel getError($errorcode)



Returns a sample error object for the given error code. Useful for designing code to react to errors when they occur for real.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\UtilsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$errorcode = "errorcode_example"; // string | The code of the error you would like returned

try {
    $result = $apiInstance->getError($errorcode);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UtilsApi->getError: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **errorcode** | **string**| The code of the error you would like returned |

### Return type

[**\Swagger\Client\Model\ExtendedErrorModel**](../Model/ExtendedErrorModel.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **test**
> \Swagger\Client\Model\TestResponse test()



Returns the customer ID to the caller

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\UtilsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->test();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UtilsApi->test: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\TestResponse**](../Model/TestResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


# Swagger\Client\UtilsApi

All URIs are relative to *https://api.thesmsworks.co.uk:8080/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**hello**](UtilsApi.md#hello) | **GET** /utils/hello | 


# **hello**
> \Swagger\Client\Model\HelloWorldResponse hello($name)



Returns 'Hello' to the caller

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\UtilsApi();
$name = "name_example"; // string | The name of the person to whom to say hello

try {
    $result = $api_instance->hello($name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UtilsApi->hello: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| The name of the person to whom to say hello | [optional]

### Return type

[**\Swagger\Client\Model\HelloWorldResponse**](../Model/HelloWorldResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


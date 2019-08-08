# Swagger\Client\AuthApi

All URIs are relative to *https://api.thesmsworks.co.uk/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**keySecret**](AuthApi.md#keysecret) | **GET** /auth/getApiKey | 
[**login**](AuthApi.md#login) | **POST** /auth/token | 

# **keySecret**
> \Swagger\Client\Model\ApiKeyResponse keySecret($customerid)



Utility method. Please generate your API key by following the instructions on your account page at https://thesmsworks.co.uk/user/login

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$customerid = "customerid_example"; // string | Utility method. Please generate your API key by following the instructions on your account page at https://thesmsworks.co.uk/user/login

try {
    $result = $apiInstance->keySecret($customerid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->keySecret: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customerid** | **string**| Utility method. Please generate your API key by following the instructions on your account page at https://thesmsworks.co.uk/user/login |

### Return type

[**\Swagger\Client\Model\ApiKeyResponse**](../Model/ApiKeyResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **login**
> \Swagger\Client\Model\TokenResponse login($body)



Generates a JSON Web Token for including in the Authorization header of all your calls to the API. This only needs to be done once. Generate the customer ID, API Key & Secret required for this call from the API Key tab your account page.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\Login(); // \Swagger\Client\Model\Login | API Key & Secret

try {
    $result = $apiInstance->login($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->login: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\Login**](../Model/Login.md)| API Key &amp; Secret |

### Return type

[**\Swagger\Client\Model\TokenResponse**](../Model/TokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


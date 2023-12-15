# OpenAPI\Client\OneTimePasswordApi

All URIs are relative to https://api.thesmsworks.co.uk/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**otpMessageidGet()**](OneTimePasswordApi.md#otpMessageidGet) | **GET** /otp/{messageid} |  |
| [**otpSendPost()**](OneTimePasswordApi.md#otpSendPost) | **POST** /otp/send |  |
| [**otpVerifyPost()**](OneTimePasswordApi.md#otpVerifyPost) | **POST** /otp/verify |  |


## `otpMessageidGet()`

```php
otpMessageidGet($messageid): \OpenAPI\Client\Model\OTPVerifyResponse
```



Retrieve an OTP by it's message ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\OneTimePasswordApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$messageid = 'messageid_example'; // string | The ID of the OTP you would like returned

try {
    $result = $apiInstance->otpMessageidGet($messageid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OneTimePasswordApi->otpMessageidGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **messageid** | **string**| The ID of the OTP you would like returned | |

### Return type

[**\OpenAPI\Client\Model\OTPVerifyResponse**](../Model/OTPVerifyResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `otpSendPost()`

```php
otpSendPost($otp): \OpenAPI\Client\Model\OTPResponse
```



Generates and sends a One-Time Password

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\OneTimePasswordApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$otp = new \OpenAPI\Client\Model\OTP(); // \OpenAPI\Client\Model\OTP | OTP properties

try {
    $result = $apiInstance->otpSendPost($otp);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OneTimePasswordApi->otpSendPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **otp** | [**\OpenAPI\Client\Model\OTP**](../Model/OTP.md)| OTP properties | |

### Return type

[**\OpenAPI\Client\Model\OTPResponse**](../Model/OTPResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `otpVerifyPost()`

```php
otpVerifyPost($passcode): \OpenAPI\Client\Model\OTPVerifyResponse
```



Generates and sends a One-Time Password

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\OneTimePasswordApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$passcode = new \OpenAPI\Client\Model\OTPVerify(); // \OpenAPI\Client\Model\OTPVerify | One-Time Password

try {
    $result = $apiInstance->otpVerifyPost($passcode);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OneTimePasswordApi->otpVerifyPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **passcode** | [**\OpenAPI\Client\Model\OTPVerify**](../Model/OTPVerify.md)| One-Time Password | |

### Return type

[**\OpenAPI\Client\Model\OTPVerifyResponse**](../Model/OTPVerifyResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

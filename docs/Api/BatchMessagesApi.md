# OpenAPI\Client\BatchMessagesApi

All URIs are relative to https://api.thesmsworks.co.uk/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**batchAnyPost()**](BatchMessagesApi.md#batchAnyPost) | **POST** /batch/any |  |
| [**batchBatchidGet()**](BatchMessagesApi.md#batchBatchidGet) | **GET** /batch/{batchid} |  |
| [**batchSchedulePost()**](BatchMessagesApi.md#batchSchedulePost) | **POST** /batch/schedule |  |
| [**batchSendPost()**](BatchMessagesApi.md#batchSendPost) | **POST** /batch/send |  |
| [**batchesScheduleBatchidDelete()**](BatchMessagesApi.md#batchesScheduleBatchidDelete) | **DELETE** /batches/schedule/{batchid} |  |


## `batchAnyPost()`

```php
batchAnyPost($messages): \OpenAPI\Client\Model\BatchMessageResponse
```



Sends a collection of unique SMS messages. Batches may contain up to 5000 messages at a time.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\BatchMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$messages = array('key' => new \stdClass); // object | An array of messages

try {
    $result = $apiInstance->batchAnyPost($messages);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchMessagesApi->batchAnyPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **messages** | **object**| An array of messages | |

### Return type

[**\OpenAPI\Client\Model\BatchMessageResponse**](../Model/BatchMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `batchBatchidGet()`

```php
batchBatchidGet($batchid): \OpenAPI\Client\Model\MessageResponse[]
```



Retrieve all messages in a batch with the given batch ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\BatchMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batchid = 'batchid_example'; // string | The ID of the batch you would like returned

try {
    $result = $apiInstance->batchBatchidGet($batchid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchMessagesApi->batchBatchidGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batchid** | **string**| The ID of the batch you would like returned | |

### Return type

[**\OpenAPI\Client\Model\MessageResponse[]**](../Model/MessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `batchSchedulePost()`

```php
batchSchedulePost($sms_message): \OpenAPI\Client\Model\ScheduledBatchResponse
```



Schedules a batch of SMS messages to be sent at the date time you specify

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\BatchMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_message = new \OpenAPI\Client\Model\BatchMessage(); // \OpenAPI\Client\Model\BatchMessage | Message properties

try {
    $result = $apiInstance->batchSchedulePost($sms_message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchMessagesApi->batchSchedulePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sms_message** | [**\OpenAPI\Client\Model\BatchMessage**](../Model/BatchMessage.md)| Message properties | |

### Return type

[**\OpenAPI\Client\Model\ScheduledBatchResponse**](../Model/ScheduledBatchResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `batchSendPost()`

```php
batchSendPost($sms_message): \OpenAPI\Client\Model\BatchMessageResponse
```



Send a single SMS message to multiple recipients.  Batches may contain up to 5000 messages at a time.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\BatchMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_message = new \OpenAPI\Client\Model\BatchMessage(); // \OpenAPI\Client\Model\BatchMessage | Message properties

try {
    $result = $apiInstance->batchSendPost($sms_message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchMessagesApi->batchSendPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sms_message** | [**\OpenAPI\Client\Model\BatchMessage**](../Model/BatchMessage.md)| Message properties | |

### Return type

[**\OpenAPI\Client\Model\BatchMessageResponse**](../Model/BatchMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `batchesScheduleBatchidDelete()`

```php
batchesScheduleBatchidDelete($batchid): \OpenAPI\Client\Model\CancelledMessageResponse
```



Cancels a scheduled SMS message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\BatchMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batchid = 'batchid_example'; // string | The ID of the batch you would like returned

try {
    $result = $apiInstance->batchesScheduleBatchidDelete($batchid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchMessagesApi->batchesScheduleBatchidDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batchid** | **string**| The ID of the batch you would like returned | |

### Return type

[**\OpenAPI\Client\Model\CancelledMessageResponse**](../Model/CancelledMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

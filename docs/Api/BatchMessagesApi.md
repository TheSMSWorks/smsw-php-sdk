# Swagger\Client\BatchMessagesApi

All URIs are relative to *https://api.thesmsworks.co.uk/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancelScheduledBatchJob**](BatchMessagesApi.md#cancelscheduledbatchjob) | **DELETE** /batches/schedule/{batchid} | 
[**getBatchById**](BatchMessagesApi.md#getbatchbyid) | **GET** /batch/{batchid} | 
[**scheduleBatch**](BatchMessagesApi.md#schedulebatch) | **POST** /batch/schedule | 
[**sendBatch**](BatchMessagesApi.md#sendbatch) | **POST** /batch/send | 

# **cancelScheduledBatchJob**
> \Swagger\Client\Model\CancelledMessageResponse cancelScheduledBatchJob($batchid)



Cancels a scheduled SMS message

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: JWT
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\BatchMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batchid = "batchid_example"; // string | The ID of the batch you would like returned

try {
    $result = $apiInstance->cancelScheduledBatchJob($batchid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchMessagesApi->cancelScheduledBatchJob: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **batchid** | **string**| The ID of the batch you would like returned |

### Return type

[**\Swagger\Client\Model\CancelledMessageResponse**](../Model/CancelledMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getBatchById**
> \Swagger\Client\Model\MessagesResponse getBatchById($batchid)



Retrieve all messages in a batch with the given batch ID

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: JWT
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\BatchMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batchid = "batchid_example"; // string | The ID of the batch you would like returned

try {
    $result = $apiInstance->getBatchById($batchid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchMessagesApi->getBatchById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **batchid** | **string**| The ID of the batch you would like returned |

### Return type

[**\Swagger\Client\Model\MessagesResponse**](../Model/MessagesResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **scheduleBatch**
> \Swagger\Client\Model\ScheduledBatchResponse scheduleBatch($body)



Schedules a batch of SMS messages to be sent at the date time you specify

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: JWT
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\BatchMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\BatchMessage(); // \Swagger\Client\Model\BatchMessage | Message properties

try {
    $result = $apiInstance->scheduleBatch($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchMessagesApi->scheduleBatch: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\BatchMessage**](../Model/BatchMessage.md)| Message properties |

### Return type

[**\Swagger\Client\Model\ScheduledBatchResponse**](../Model/ScheduledBatchResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **sendBatch**
> \Swagger\Client\Model\BatchMessageResponse sendBatch($body)



Send a single SMS message to multiple recipients

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: JWT
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\BatchMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\BatchMessage(); // \Swagger\Client\Model\BatchMessage | Message properties

try {
    $result = $apiInstance->sendBatch($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchMessagesApi->sendBatch: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\BatchMessage**](../Model/BatchMessage.md)| Message properties |

### Return type

[**\Swagger\Client\Model\BatchMessageResponse**](../Model/BatchMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


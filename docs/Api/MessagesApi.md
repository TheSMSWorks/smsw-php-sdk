# Swagger\Client\MessagesApi

All URIs are relative to *https://api.thesmsworks.co.uk/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancelScheduledJob**](MessagesApi.md#cancelScheduledJob) | **DELETE** /messages/schedule/{messageid} | 
[**getMessageById**](MessagesApi.md#getMessageById) | **GET** /messages/{messageid} | 
[**getMessages**](MessagesApi.md#getMessages) | **POST** /messages | 
[**scheduleMessage**](MessagesApi.md#scheduleMessage) | **POST** /message/schedule | 
[**sendMessage**](MessagesApi.md#sendMessage) | **POST** /message/send | 


# **cancelScheduledJob**
> \Swagger\Client\Model\CancelledMessageResponse cancelScheduledJob($messageid)



Cancels a scheduled SMS message

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: JWT
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$api_instance = new Swagger\Client\Api\MessagesApi();
$messageid = "messageid_example"; // string | The ID of the message you would like returned

try {
    $result = $api_instance->cancelScheduledJob($messageid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->cancelScheduledJob: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **messageid** | **string**| The ID of the message you would like returned |

### Return type

[**\Swagger\Client\Model\CancelledMessageResponse**](../Model/CancelledMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMessageById**
> \Swagger\Client\Model\MessageResponse getMessageById($messageid)



Retrieve a logged message by the message ID

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: JWT
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$api_instance = new Swagger\Client\Api\MessagesApi();
$messageid = "messageid_example"; // string | The ID of the message you would like returned

try {
    $result = $api_instance->getMessageById($messageid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->getMessageById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **messageid** | **string**| The ID of the message you would like returned |

### Return type

[**\Swagger\Client\Model\MessageResponse**](../Model/MessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMessages**
> \Swagger\Client\Model\MessagesResponse getMessages($query)



Get messages matching your search criteria

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: JWT
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$api_instance = new Swagger\Client\Api\MessagesApi();
$query = new \Swagger\Client\Model\Query(); // \Swagger\Client\Model\Query | 

try {
    $result = $api_instance->getMessages($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->getMessages: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**\Swagger\Client\Model\Query**](../Model/Query.md)|  |

### Return type

[**\Swagger\Client\Model\MessagesResponse**](../Model/MessagesResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **scheduleMessage**
> \Swagger\Client\Model\ScheduledMessageResponse scheduleMessage($sms_message)



Schedules an SMS message to be sent at the date-time you specify

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: JWT
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$api_instance = new Swagger\Client\Api\MessagesApi();
$sms_message = new \Swagger\Client\Model\Message(); // \Swagger\Client\Model\Message | Message properties

try {
    $result = $api_instance->scheduleMessage($sms_message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->scheduleMessage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sms_message** | [**\Swagger\Client\Model\Message**](../Model/Message.md)| Message properties |

### Return type

[**\Swagger\Client\Model\ScheduledMessageResponse**](../Model/ScheduledMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **sendMessage**
> \Swagger\Client\Model\SendMessageResponse sendMessage($sms_message)



Sends an SMS message

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: JWT
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$api_instance = new Swagger\Client\Api\MessagesApi();
$sms_message = new \Swagger\Client\Model\Message(); // \Swagger\Client\Model\Message | Message properties

try {
    $result = $api_instance->sendMessage($sms_message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->sendMessage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sms_message** | [**\Swagger\Client\Model\Message**](../Model/Message.md)| Message properties |

### Return type

[**\Swagger\Client\Model\SendMessageResponse**](../Model/SendMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json;charset=UTF-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


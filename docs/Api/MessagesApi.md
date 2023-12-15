# OpenAPI\Client\MessagesApi

All URIs are relative to https://api.thesmsworks.co.uk/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**messageSchedulePost()**](MessagesApi.md#messageSchedulePost) | **POST** /message/schedule |  |
| [**messageSendPost()**](MessagesApi.md#messageSendPost) | **POST** /message/send |  |
| [**messagesFailedPost()**](MessagesApi.md#messagesFailedPost) | **POST** /messages/failed |  |
| [**messagesInboxPost()**](MessagesApi.md#messagesInboxPost) | **POST** /messages/inbox |  |
| [**messagesMessageidDelete()**](MessagesApi.md#messagesMessageidDelete) | **DELETE** /messages/{messageid} |  |
| [**messagesMessageidGet()**](MessagesApi.md#messagesMessageidGet) | **GET** /messages/{messageid} |  |
| [**messagesPost()**](MessagesApi.md#messagesPost) | **POST** /messages |  |
| [**messagesScheduleGet()**](MessagesApi.md#messagesScheduleGet) | **GET** /messages/schedule |  |
| [**messagesScheduleMessageidDelete()**](MessagesApi.md#messagesScheduleMessageidDelete) | **DELETE** /messages/schedule/{messageid} |  |
| [**sendFlashMessage()**](MessagesApi.md#sendFlashMessage) | **POST** /message/flash |  |


## `messageSchedulePost()`

```php
messageSchedulePost($sms_message): \OpenAPI\Client\Model\ScheduledMessageResponse[]
```



Schedules an SMS message to be sent at the date-time you specify

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_message = new \OpenAPI\Client\Model\Message(); // \OpenAPI\Client\Model\Message | Message properties

try {
    $result = $apiInstance->messageSchedulePost($sms_message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messageSchedulePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sms_message** | [**\OpenAPI\Client\Model\Message**](../Model/Message.md)| Message properties | |

### Return type

[**\OpenAPI\Client\Model\ScheduledMessageResponse[]**](../Model/ScheduledMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messageSendPost()`

```php
messageSendPost($sms_message): \OpenAPI\Client\Model\SendMessageResponse
```



Send an SMS Message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_message = new \OpenAPI\Client\Model\Message(); // \OpenAPI\Client\Model\Message | Message properties

try {
    $result = $apiInstance->messageSendPost($sms_message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messageSendPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sms_message** | [**\OpenAPI\Client\Model\Message**](../Model/Message.md)| Message properties | |

### Return type

[**\OpenAPI\Client\Model\SendMessageResponse**](../Model/SendMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesFailedPost()`

```php
messagesFailedPost($query): \OpenAPI\Client\Model\MessageResponse[]
```



Get failed messages matching your search criteria

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = new \OpenAPI\Client\Model\Query(); // \OpenAPI\Client\Model\Query

try {
    $result = $apiInstance->messagesFailedPost($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesFailedPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | [**\OpenAPI\Client\Model\Query**](../Model/Query.md)|  | |

### Return type

[**\OpenAPI\Client\Model\MessageResponse[]**](../Model/MessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesInboxPost()`

```php
messagesInboxPost($query): \OpenAPI\Client\Model\MessageResponse[]
```



Get unread uncoming messages matching your search criteria

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = new \OpenAPI\Client\Model\Query(); // \OpenAPI\Client\Model\Query

try {
    $result = $apiInstance->messagesInboxPost($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesInboxPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | [**\OpenAPI\Client\Model\Query**](../Model/Query.md)|  | |

### Return type

[**\OpenAPI\Client\Model\MessageResponse[]**](../Model/MessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesMessageidDelete()`

```php
messagesMessageidDelete($messageid): \OpenAPI\Client\Model\DeletedMessageResponse
```



Delete the message with the mathcing messageid

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$messageid = 'messageid_example'; // string | The ID of the message you would like returned

try {
    $result = $apiInstance->messagesMessageidDelete($messageid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesMessageidDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **messageid** | **string**| The ID of the message you would like returned | |

### Return type

[**\OpenAPI\Client\Model\DeletedMessageResponse**](../Model/DeletedMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesMessageidGet()`

```php
messagesMessageidGet($messageid): \OpenAPI\Client\Model\MessageResponse
```



Retrieve a logged message by the message ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$messageid = 'messageid_example'; // string | The ID of the message you would like returned

try {
    $result = $apiInstance->messagesMessageidGet($messageid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesMessageidGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **messageid** | **string**| The ID of the message you would like returned | |

### Return type

[**\OpenAPI\Client\Model\MessageResponse**](../Model/MessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesPost()`

```php
messagesPost($query): \OpenAPI\Client\Model\MessageResponse[]
```



Retrieve up to 1000 messages matching your search criteria

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = new \OpenAPI\Client\Model\Query(); // \OpenAPI\Client\Model\Query

try {
    $result = $apiInstance->messagesPost($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **query** | [**\OpenAPI\Client\Model\Query**](../Model/Query.md)|  | |

### Return type

[**\OpenAPI\Client\Model\MessageResponse[]**](../Model/MessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesScheduleGet()`

```php
messagesScheduleGet(): \OpenAPI\Client\Model\ScheduledMessagesResponse
```



Returns a list of messages scheduled from your account, comprising any messages scheduled in the last 3 months and any scheduled to send in the future

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->messagesScheduleGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesScheduleGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\ScheduledMessagesResponse**](../Model/ScheduledMessagesResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesScheduleMessageidDelete()`

```php
messagesScheduleMessageidDelete($messageid): \OpenAPI\Client\Model\CancelledMessageResponse
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


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$messageid = 'messageid_example'; // string | The ID of the message you would like returned

try {
    $result = $apiInstance->messagesScheduleMessageidDelete($messageid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesScheduleMessageidDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **messageid** | **string**| The ID of the message you would like returned | |

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

## `sendFlashMessage()`

```php
sendFlashMessage($sms_message): \OpenAPI\Client\Model\SendMessageResponse
```



Sends an SMS flash message, which appears on the recipients lock screen

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_message = new \OpenAPI\Client\Model\Message(); // \OpenAPI\Client\Model\Message | Message properties

try {
    $result = $apiInstance->sendFlashMessage($sms_message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->sendFlashMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sms_message** | [**\OpenAPI\Client\Model\Message**](../Model/Message.md)| Message properties | |

### Return type

[**\OpenAPI\Client\Model\SendMessageResponse**](../Model/SendMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

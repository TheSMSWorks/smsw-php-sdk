# The SMSWorks PHP SDK

The SMS Works provides a low-cost, reliable [SMS API for developers](https://thesmsworks.co.uk/). Pay only for delivered texts, all failed messages are refunded.

This package is a fork of the <a href="https://github.com/TheSMSWorks/smsw-php-sdk">PHP SDK for the SMS Works Message API</a>,
forked to be compatible with Laravel 10.x. We don't recommend you use this package since we will remove it once the parent
package has itself been updated by TheSMSWorks.


## Requirements

PHP 8.1 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/ssiva13/smsw-php-sdk.git"
    }
  ],
  "require": {
    "ssiva/smsw-php-sdk": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to *https://api.thesmsworks.co.uk/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthApi* | [**keySecret**](docs/Api/AuthApi.md#keysecret) | **GET** /auth/getApiKey |
*AuthApi* | [**login**](docs/Api/AuthApi.md#login) | **POST** /auth/token |
*BatchMessagesApi* | [**cancelScheduledBatchJob**](docs/Api/BatchMessagesApi.md#cancelscheduledbatchjob) | **DELETE** /batches/schedule/{batchid} |
*BatchMessagesApi* | [**getBatchById**](docs/Api/BatchMessagesApi.md#getbatchbyid) | **GET** /batch/{batchid} |
*BatchMessagesApi* | [**scheduleBatch**](docs/Api/BatchMessagesApi.md#schedulebatch) | **POST** /batch/schedule |
*BatchMessagesApi* | [**sendBatch**](docs/Api/BatchMessagesApi.md#sendbatch) | **POST** /batch/send |
*CreditsApi* | [**credits**](docs/Api/CreditsApi.md#credits) | **GET** /credits/balance |
*MessagesApi* | [**cancelScheduledJob**](docs/Api/MessagesApi.md#cancelscheduledjob) | **DELETE** /messages/schedule/{messageid} |
*MessagesApi* | [**getInboxMessages**](docs/Api/MessagesApi.md#getinboxmessages) | **POST** /messages/inbox |
*MessagesApi* | [**getMessageById**](docs/Api/MessagesApi.md#getmessagebyid) | **GET** /messages/{messageid} |
*MessagesApi* | [**getMessages**](docs/Api/MessagesApi.md#getmessages) | **POST** /messages |
*MessagesApi* | [**scheduleMessage**](docs/Api/MessagesApi.md#schedulemessage) | **POST** /message/schedule |
*MessagesApi* | [**sendMessage**](docs/Api/MessagesApi.md#sendmessage) | **POST** /message/send |
*UtilsApi* | [**getError**](docs/Api/UtilsApi.md#geterror) | **GET** /utils/errors/{errorcode} |
*UtilsApi* | [**test**](docs/Api/UtilsApi.md#test) | **GET** /utils/test |

## Documentation For Models

 - [ApiKeyResponse](docs/Model/ApiKeyResponse.md)
 - [BatchMessage](docs/Model/BatchMessage.md)
 - [BatchMessageResponse](docs/Model/BatchMessageResponse.md)
 - [CancelledMessageResponse](docs/Model/CancelledMessageResponse.md)
 - [CreditsResponse](docs/Model/CreditsResponse.md)
 - [ErrorModel](docs/Model/ErrorModel.md)
 - [ExtendedErrorModel](docs/Model/ExtendedErrorModel.md)
 - [Login](docs/Model/Login.md)
 - [Message](docs/Model/Message.md)
 - [MessageResponse](docs/Model/MessageResponse.md)
 - [MessagesResponse](docs/Model/MessagesResponse.md)
 - [MetaData](docs/Model/MetaData.md)
 - [Query](docs/Model/Query.md)
 - [ScheduledBatchResponse](docs/Model/ScheduledBatchResponse.md)
 - [ScheduledMessageResponse](docs/Model/ScheduledMessageResponse.md)
 - [SendMessageResponse](docs/Model/SendMessageResponse.md)
 - [TestResponse](docs/Model/TestResponse.md)
 - [TokenResponse](docs/Model/TokenResponse.md)

## Documentation For Authorization


## JWT

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header



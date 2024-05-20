# OpenAPIClient-php

The SMS Works provides a low-cost, reliable SMS API for developers. Pay only for delivered texts, all failed UK messages are refunded.

For more information, please visit [https://thesmsworks.co.uk/contact](https://thesmsworks.co.uk/contact).

## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/thesmsworks/smsw-php-sdk.git"
    }
  ],
  "require": {
    "thesmsworks/smsw-php-sdk": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## API Endpoints

All URIs are relative to *https://api.thesmsworks.co.uk/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BatchMessagesApi* | [**batchAnyPost**](docs/Api/BatchMessagesApi.md#batchanypost) | **POST** /batch/any | 
*BatchMessagesApi* | [**batchBatchidGet**](docs/Api/BatchMessagesApi.md#batchbatchidget) | **GET** /batch/{batchid} | 
*BatchMessagesApi* | [**batchSchedulePost**](docs/Api/BatchMessagesApi.md#batchschedulepost) | **POST** /batch/schedule | 
*BatchMessagesApi* | [**batchSendPost**](docs/Api/BatchMessagesApi.md#batchsendpost) | **POST** /batch/send | 
*BatchMessagesApi* | [**batchesScheduleBatchidDelete**](docs/Api/BatchMessagesApi.md#batchesschedulebatchiddelete) | **DELETE** /batches/schedule/{batchid} | 
*CreditsApi* | [**creditsBalanceGet**](docs/Api/CreditsApi.md#creditsbalanceget) | **GET** /credits/balance | 
*MessagesApi* | [**messageSchedulePost**](docs/Api/MessagesApi.md#messageschedulepost) | **POST** /message/schedule | 
*MessagesApi* | [**messageSendPost**](docs/Api/MessagesApi.md#messagesendpost) | **POST** /message/send | 
*MessagesApi* | [**messagesFailedPost**](docs/Api/MessagesApi.md#messagesfailedpost) | **POST** /messages/failed | 
*MessagesApi* | [**messagesInboxPost**](docs/Api/MessagesApi.md#messagesinboxpost) | **POST** /messages/inbox | 
*MessagesApi* | [**messagesMessageidDelete**](docs/Api/MessagesApi.md#messagesmessageiddelete) | **DELETE** /messages/{messageid} | 
*MessagesApi* | [**messagesMessageidGet**](docs/Api/MessagesApi.md#messagesmessageidget) | **GET** /messages/{messageid} | 
*MessagesApi* | [**messagesPost**](docs/Api/MessagesApi.md#messagespost) | **POST** /messages | 
*MessagesApi* | [**messagesScheduleGet**](docs/Api/MessagesApi.md#messagesscheduleget) | **GET** /messages/schedule | 
*MessagesApi* | [**messagesScheduleMessageidDelete**](docs/Api/MessagesApi.md#messagesschedulemessageiddelete) | **DELETE** /messages/schedule/{messageid} | 
*MessagesApi* | [**sendFlashMessage**](docs/Api/MessagesApi.md#sendflashmessage) | **POST** /message/flash | 
*OneTimePasswordApi* | [**otpMessageidGet**](docs/Api/OneTimePasswordApi.md#otpmessageidget) | **GET** /otp/{messageid} | 
*OneTimePasswordApi* | [**otpSendPost**](docs/Api/OneTimePasswordApi.md#otpsendpost) | **POST** /otp/send | 
*OneTimePasswordApi* | [**otpVerifyPost**](docs/Api/OneTimePasswordApi.md#otpverifypost) | **POST** /otp/verify | 
*UtilsApi* | [**utilsErrorsErrorcodeGet**](docs/Api/UtilsApi.md#utilserrorserrorcodeget) | **GET** /utils/errors/{errorcode} | 
*UtilsApi* | [**utilsTestGet**](docs/Api/UtilsApi.md#utilstestget) | **GET** /utils/test | 

## Models

- [BatchMessage](docs/Model/BatchMessage.md)
- [BatchMessageResponse](docs/Model/BatchMessageResponse.md)
- [CancelledMessageResponse](docs/Model/CancelledMessageResponse.md)
- [CreditsResponse](docs/Model/CreditsResponse.md)
- [DeletedMessageResponse](docs/Model/DeletedMessageResponse.md)
- [ErrorModel](docs/Model/ErrorModel.md)
- [ExtendedErrorModel](docs/Model/ExtendedErrorModel.md)
- [Message](docs/Model/Message.md)
- [MessageMetadata](docs/Model/MessageMetadata.md)
- [MessageResponse](docs/Model/MessageResponse.md)
- [MessageResponseFailurereason](docs/Model/MessageResponseFailurereason.md)
- [MetaData](docs/Model/MetaData.md)
- [OTP](docs/Model/OTP.md)
- [OTPResponse](docs/Model/OTPResponse.md)
- [OTPVerify](docs/Model/OTPVerify.md)
- [OTPVerifyResponse](docs/Model/OTPVerifyResponse.md)
- [Query](docs/Model/Query.md)
- [QueryMetadata](docs/Model/QueryMetadata.md)
- [ScheduledBatchResponse](docs/Model/ScheduledBatchResponse.md)
- [ScheduledMessage](docs/Model/ScheduledMessage.md)
- [ScheduledMessageResponse](docs/Model/ScheduledMessageResponse.md)
- [ScheduledMessagesResponse](docs/Model/ScheduledMessagesResponse.md)
- [ScheduledMessagesResponseMessage](docs/Model/ScheduledMessagesResponseMessage.md)
- [SendMessageResponse](docs/Model/SendMessageResponse.md)
- [TestResponse](docs/Model/TestResponse.md)

## Authorization

Authentication schemes defined for the API:
### JWT

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author

support@thesmsworks.co.uk

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.9.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`

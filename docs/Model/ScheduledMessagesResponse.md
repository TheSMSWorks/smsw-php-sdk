# # ScheduledMessagesResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **string** | The status of the scheduled message (either &#39;SCHEDULED&#39;, &#39;PROCESSED&#39; or &#39;CANCELLED&#39;) | [optional]
**id** | **string** | The scheduled message ID | [optional]
**batch** | **bool** | Describes whether the a batch of messages has been scheduled, or just a single message | [optional]
**message** | [**\OpenAPI\Client\Model\ScheduledMessagesResponseMessage**](ScheduledMessagesResponseMessage.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

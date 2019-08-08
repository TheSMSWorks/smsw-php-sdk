# Query

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **string** | The status of the messages you would like returned (either &#x27;SENT&#x27;, &#x27;DELIVERED&#x27;, &#x27;EXPIRED&#x27;, &#x27;UNDELIVERABLE&#x27;, &#x27;REJECTED&#x27; or &#x27;INCOMING&#x27;) | [optional] 
**credits** | [**float**](float.md) | The number of credits used on the message | [optional] 
**destination** | **string** | The phone number of the recipient. Start UK numbers with 44 and drop the leading 0. | [optional] 
**sender** | **string** | The sender of the message (this can be the configured sender name for an outbound message or the senders phone number for an inbound message). | [optional] 
**keyword** | **string** | The keyword used in the inbound message | [optional] 
**from** | **string** | The date-time from which you would like matching messages | [optional] 
**to** | **string** | The date-time to which you would like matching messages | [optional] 
**metadata** | **object** | An array of objects containing metadata key/value pairs that have been saved on messages. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


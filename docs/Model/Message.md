# Message

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sender** | **string** | The sender of the message. Should be no longer than 11 characters for alphanumeric or 15 characters for numeric sender ID&#39;s. No spaces or special characters. | 
**destination** | **string** | Telephone number of the recipient | 
**content** | **string** | Message to send to the recipient. Content can be up to 640 characters in length. You will be charged 1 credit for each 160 characters, up to a maximum of 4 credits. Messages sent to numbers registered outside the UK will be charged double credits (i.e. 2 credits per 160 characters, up to maximum of 8 credits). | 
**schedule** | **string** | Date at which to send the message. This is only used by the message/schedule service and can be left empty for other services. | 
**tag** | **string** | An identifying label for the message, which you can use to filter and report on messages you&#39;ve sent later. Ideal for campaigns. | [optional] 
**ttl** | **float** | The number of minutes before the message is deleted. Optional. Omit to prevent delivery report deletion. | [optional] 
**metadata** | [**\Swagger\Client\Model\MessageMetadata**](MessageMetadata.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



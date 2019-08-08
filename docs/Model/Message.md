# Message

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sender** | **string** | The sender of the message. Should be no longer than 11 characters for alphanumeric or 15 characters for numeric sender ID&#x27;s. No spaces or special characters. | 
**destination** | **string** | Telephone number of the recipient | 
**content** | **string** | Message to send to the recipient. Content can be up to 1280 characters in length. You will be charged 1 credit for each 160 characters, up to a maximum of 8 credits. Messages sent to numbers registered outside the UK will be charged double credits (i.e. 2 credits per 160 characters, up to maximum of 8 credits). | 
**schedule** | **string** | Date at which to send the message. This is only used by the message/schedule service and can be left empty for other services. | [optional] 
**tag** | **string** | An identifying label for the message, which you can use to filter and report on messages you&#x27;ve sent later. Ideal for campaigns. A maximum of 280 characters. | [optional] 
**ttl** | [**float**](float.md) | The optional number of minutes before the message is deleted. Optional. Omit to prevent delivery report deletion. | [optional] 
**responseemail** | **string[]** | An optional list of email addresses to forward responses to this specific message to. An SMS Works Reply Number is required to use this feature. | [optional] 
**metadata** | **object** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


# # BatchMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sender** | **string** | The sender of the message. Should be no longer than 11 characters for alphanumeric or 15 characters for numeric sender ID&#39;s. No spaces or special characters. |
**destinations** | **string[]** | Telephone numbers of each of the recipients |
**content** | **string** | Message to send to the recipient |
**deliveryreporturl** | **string** | The url to which we should POST delivery reports to for this message. If none is specified, we&#39;ll use the global delivery report URL that you&#39;ve configured on your account page. | [optional]
**schedule** | **string** | Date-time at which to send the batch. This is only used by the batch/schedule service. | [optional]
**tag** | **string** | An identifying label for the message, which you can use to filter and report on messages you&#39;ve sent later. Ideal for campaigns. A maximum of 280 characters. | [optional]
**ttl** | **float** | The number of minutes before the delivery report is deleted. Optional. Omit to prevent delivery report deletion. Integer. | [optional]
**validity** | **float** | The optional number of minutes to attempt delivery before the message is marked as EXPIRED. Optional. The default is 2880 minutes. Integer. | [optional]
**ai** | **bool** | Used to determine whether The SMS Works AI Optimiser should be used in the event that the message is just longer than the 1 or 2 credit boundary. This setting overrides the AI Optimiser configuration on your SMS Works account. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

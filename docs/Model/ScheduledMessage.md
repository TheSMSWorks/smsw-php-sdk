# # ScheduledMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sender** | **string** | The sender of the message. Should be no longer than 11 characters for alphanumeric or 15 characters for numeric sender ID&#39;s. No spaces or special characters. | [optional]
**content** | **string** | Message to be sent to the recipient | [optional]
**destination** | **string** | For single scheduled messages, the mobile number of the recipient | [optional]
**destinations** | **string[]** | For batch messages, the mobile numbers of each of the recipients | [optional]
**schedule** | **string** | Date-time at which to send the batch. This is only used by the batch/schedule service. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

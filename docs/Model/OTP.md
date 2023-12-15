# # OTP

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sender** | **string** | The sender of the message. Should be no longer than 11 characters for alphanumeric or 15 characters for numeric sender ID&#39;s. No spaces or special characters. | [optional]
**destination** | **string** | The phone number of the recipient. | [optional]
**length** | **object** | The length of the generated passcode. The default length is 6 characters, which will apply if this parameter is omitted. All generated passcodes are numeric. Optional. | [optional]
**template** | **string** | A template to use as the content for the message. You must include the &#39;{{passcode}}&#39; placeholder, which will be replaced by the generated passcode when the message is sent. Optional. | [optional]
**validity** | **float** | The length of time in seconds for which the generated passcode should be valid. Optional. | [optional]
**passcode** | **string** | A passcode you supply for use in the message template. This will be stored on the OTP record in our system for later verification. Optional. | [optional]
**metadata** | **object** | A JSON object of no longer than 1024 bytes, containing as many parameters as you wish, to store data for use in your application. This will be returned when you verify the passcode. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

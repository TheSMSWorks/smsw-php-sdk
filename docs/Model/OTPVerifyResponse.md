# # OTPVerifyResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**destination** | **string** | The mobile number that the OTP was sent to | [optional]
**status** | **string** | The status of the OTP. If the passcode is used within the validity period then this will be &#39;VERIFIED&#39;, otherwise it will be &#39;EXPIRED&#39; | [optional]
**passcode** | **float** | The passcode used. | [optional]
**validity** | **float** | The length of time in seconds for which the generated passcode is valid. | [optional]
**metadata** | **object** | A JSON object storing data supplied when this passcode was generated, for use in your application. | [optional]
**created** | **string** | The ISO 8601 date/time at which this OTP was created | [optional]
**expires** | **string** | The ISO 8601 date/time at which this OTP expires | [optional]
**modified** | **string** | The ISO 8601 date/time at which this OTP was modified (typically when it was verified) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

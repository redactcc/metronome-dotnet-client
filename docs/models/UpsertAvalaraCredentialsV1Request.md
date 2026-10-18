# Org.OpenAPITools.Model.UpsertAvalaraCredentialsV1Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DeliveryMethodIds** | **List&lt;string&gt;** | The delivery method IDs of the billing provider configurations to update, can be found in the response of the &#x60;/listConfiguredBillingProviders&#x60; endpoint. | 
**AvalaraEnvironment** | **string** | The Avalara environment to use (SANDBOX or PRODUCTION). | 
**AvalaraUsername** | **string** | The username for the Avalara account. | 
**AvalaraPassword** | **string** | The password for the Avalara account. | 
**CommitTransactions** | **bool** | Commit transactions if you want Metronome tax calculations used for reporting and tax filings. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


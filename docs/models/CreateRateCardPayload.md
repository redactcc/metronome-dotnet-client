# Org.OpenAPITools.Model.CreateRateCardPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Used only in UI/API. It is not exposed to end customers. | 
**Description** | **string** |  | [optional] 
**FiatCreditTypeId** | **Guid** | The Metronome ID of the credit type to associate with the rate card, defaults to USD (cents) if not passed. | [optional] 
**CreditTypeConversions** | [**List&lt;CreditTypeConversionInput&gt;**](CreditTypeConversionInput.md) | Required when using custom pricing units in rates. | [optional] 
**Aliases** | [**List&lt;RateCardAlias&gt;**](RateCardAlias.md) | Reference this alias when creating a contract. If the same alias is assigned to multiple rate cards, it will reference the rate card to which it was most recently assigned. It is not exposed to end customers. | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


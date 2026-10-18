# Org.OpenAPITools.Model.UpdateRateCardPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RateCardId** | **Guid** | ID of the rate card to update | 
**Name** | **string** | Used only in UI/API. It is not exposed to end customers. | [optional] 
**Description** | **string** |  | [optional] 
**Aliases** | [**List&lt;RateCardAlias&gt;**](RateCardAlias.md) | Reference this alias when creating a contract. If the same alias is assigned to multiple rate cards, it will reference the rate card to which it was most recently assigned. It is not exposed to end customers. | [optional] 
**AddCreditTypeConversions** | [**List&lt;CreditTypeConversionInput&gt;**](CreditTypeConversionInput.md) | Add credit type conversions for using custom pricing units in rates. Existing conversions cannot be modified. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


# Org.OpenAPITools.Model.SetCustomerBillableStatusPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** |  | 
**BillableStatus** | **BillableStatus** |  | 
**EffectiveAt** | **DateTime** | For usage invoices, any invoices where the service periods starts on or after this date will be included. For all other invoice types, only invoices where the issue_date falls on or after this date will be included. | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


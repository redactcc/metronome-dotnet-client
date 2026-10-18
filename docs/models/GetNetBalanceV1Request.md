# Org.OpenAPITools.Model.GetNetBalanceV1Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | The ID of the customer. | 
**CreditTypeId** | **Guid** | The ID of the credit type (can be fiat or a custom pricing unit) to get the balance for. Defaults to USD (cents) if not specified. | [optional] 
**AccessType** | **string** | Filters balances by how they are drawn down. Defaults to &#x60;SPEND&#x60;. If set to &#x60;QUANTITY&#x60;, &#x60;credit_type_id&#x60; must not be provided. | [optional] 
**Filters** | [**List&lt;BalanceFilter&gt;**](BalanceFilter.md) | Balance filters are OR&#39;d together, so if a given commit or credit matches any of the filters, it will be included in the net balance. | [optional] 
**InvoiceInclusionMode** | **string** | Controls which invoices are considered when calculating the remaining balance. &#x60;FINALIZED&#x60; considers only deductions from finalized invoices. &#x60;FINALIZED_AND_DRAFT&#x60; also includes deductions from pending draft invoices. | [optional] [default to InvoiceInclusionModeEnum.FINALIZEDANDDRAFT]

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


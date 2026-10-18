# Org.OpenAPITools.Model.AmendContractPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | ID of the customer whose contract is to be amended | 
**ContractId** | **Guid** | ID of the contract to amend | 
**StartingAt** | **DateTime** | inclusive start time for the amendment | 
**NetsuiteSalesOrderId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**SalesforceOpportunityId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**TotalContractValue** | **decimal** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**Commits** | [**List&lt;CommitInput&gt;**](CommitInput.md) |  | [optional] 
**Credits** | [**List&lt;CreditInput&gt;**](CreditInput.md) |  | [optional] 
**Overrides** | [**List&lt;OverrideInput&gt;**](OverrideInput.md) |  | [optional] 
**Discounts** | [**List&lt;DiscountInput&gt;**](DiscountInput.md) | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**ProfessionalServices** | [**List&lt;ProServiceInput&gt;**](ProServiceInput.md) | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**ResellerRoyalties** | [**List&lt;ResellerRoyaltyOrUpdateInput&gt;**](ResellerRoyaltyOrUpdateInput.md) | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**ScheduledCharges** | [**List&lt;ScheduledChargeInput&gt;**](ScheduledChargeInput.md) |  | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


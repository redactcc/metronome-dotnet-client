# Org.OpenAPITools.Model.CreateCustomerPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | This will be truncated to 160 characters if the provided name is longer. | 
**IngestAliases** | **List&lt;string&gt;** | Aliases that can be used to refer to this customer in usage events | [optional] 
**CustomerBillingProviderConfigurations** | [**List&lt;CustomerBillingProviderConfigurationCreateCustomerInput&gt;**](CustomerBillingProviderConfigurationCreateCustomerInput.md) |  | [optional] 
**CustomerRevenueSystemConfigurations** | [**List&lt;CustomerRevenueSystemConfigurationCreateCustomerInput&gt;**](CustomerRevenueSystemConfigurationCreateCustomerInput.md) |  | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


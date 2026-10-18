# Org.OpenAPITools.Model.CustomerBillingProviderConfigurationCreateCustomerInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BillingProvider** | **ContractsBillingProviderType** |  | 
**TaxProvider** | **TaxProviderType** |  | [optional] 
**VarConfiguration** | **Dictionary&lt;string, Object&gt;** | Configuration for the billing provider. The structure of this object is specific to the billing provider and delivery provider combination. Defaults to an empty object, however, for most billing provider + delivery method combinations, it will not be a valid configuration. | [optional] 
**DeliveryMethodId** | **Guid** | ID of the delivery method to use for this customer. If not provided, the &#x60;delivery_method&#x60; must be provided. | [optional] 
**DeliveryMethod** | **BillingProviderDeliveryMethodType** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


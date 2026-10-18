# Org.OpenAPITools.Model.CustomerBillingProviderConfigurationLookup
The billing provider configuration associated with a contract. Provide either an ID or the provider and delivery method.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BillingProviderConfigurationId** | **Guid** | The Metronome ID of the billing provider configuration. Use when a customer has multiple configurations with the same billing provider and delivery method. Otherwise, specify the billing_provider and delivery_method. | [optional] 
**BillingProvider** | **ContractsBillingProviderType** |  | [optional] 
**DeliveryMethod** | **BillingProviderDeliveryMethodType** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


# Org.OpenAPITools.Model.CustomerBillingProviderConfiguration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | ID of this configuration; can be provided as the billing_provider_configuration_id when creating a contract. | 
**BillingProvider** | **BillingProviderType** |  | 
**CustomerId** | **Guid** |  | 
**VarConfiguration** | **Dictionary&lt;string, Object&gt;** | Configuration for the billing provider. The structure of this object is specific to the billing provider. | 
**DeliveryMethodId** | **Guid** | ID of the delivery method to use for this customer. | 
**DeliveryMethod** | **BillingProviderDeliveryMethodType** |  | 
**DeliveryMethodConfiguration** | **Dictionary&lt;string, Object&gt;** | Configuration for the delivery method. The structure of this object is specific to the delivery method. | 
**ArchivedAt** | **DateTime** |  | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


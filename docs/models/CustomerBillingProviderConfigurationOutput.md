# Org.OpenAPITools.Model.CustomerBillingProviderConfigurationOutput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | ID of the created configuration | [optional] 
**BillingProvider** | **BillingProviderType** |  | [optional] 
**CustomerId** | **Guid** | ID of the customer this configuration is associated with. | [optional] 
**VarConfiguration** | **Dictionary&lt;string, Object&gt;** | Configuration for the billing provider. The structure of this object is specific to the billing provider and delivery method combination. | [optional] 
**DeliveryMethodId** | **Guid** | ID of the delivery method used for this customer configuration. | [optional] 
**TaxProvider** | **TaxProviderType** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


# Org.OpenAPITools.Model.CustomerBillingProviderConfigurationInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BillingProvider** | **BillingProviderType** |  | 
**CustomerId** | **Guid** |  | 
**TaxProvider** | **TaxProviderType** |  | [optional] 
**VarConfiguration** | **Dictionary&lt;string, Object&gt;** | Configuration for the billing provider. The structure of this object is specific to the billing provider and delivery method combination. Defaults to an empty object, however, for most billing provider + delivery method combinations, it will not be a valid configuration.  For AWS marketplace configurations, the aws_is_subscription_product flag can be used to indicate a product with usage-based pricing.  More information can be found [here](https://docs.metronome.com/invoice-customers/solutions/marketplaces/invoice-aws/#provision-aws-marketplace-customers-in-metronome). | [optional] 
**DeliveryMethodId** | **Guid** | ID of the delivery method to use for this customer. If not provided, the &#x60;delivery_method&#x60; must be provided. | [optional] 
**DeliveryMethod** | **BillingProviderDeliveryMethodType** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


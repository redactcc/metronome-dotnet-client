# Org.OpenAPITools.Model.CustomerRevenueSystemConfigurationLookup
The revenue system configuration associated with a contract. Provide either an ID or the provider and delivery method.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RevenueSystemConfigurationId** | **Guid** | The Metronome ID of the revenue system configuration. Use when a customer has multiple configurations with the same provider and delivery method. Otherwise, specify the provider and delivery_method. | [optional] 
**Provider** | **RevenueSystemProviderType** |  | [optional] 
**DeliveryMethod** | **RevenueSystemDeliveryMethodType** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


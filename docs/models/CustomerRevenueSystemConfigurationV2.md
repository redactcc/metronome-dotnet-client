# Org.OpenAPITools.Model.CustomerRevenueSystemConfigurationV2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | ID of the revenue system configuration. | 
**CustomerId** | **Guid** |  | 
**DeliveryMethodId** | **Guid** | ID of the delivery method used for this customer configuration. | 
**Provider** | **RevenueSystemProviderTypeV2** |  | 
**VarConfiguration** | **Dictionary&lt;string, Object&gt;** | Configuration for the revenue system. The structure of this object is specific to the provider. | 
**DeliveryMethod** | **BillingProviderDeliveryMethodType** |  | [optional] 
**DeliveryMethodConfiguration** | **Dictionary&lt;string, Object&gt;** | Configuration for the delivery method. The structure of this object is specific to the delivery method. | [optional] 
**ArchivedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


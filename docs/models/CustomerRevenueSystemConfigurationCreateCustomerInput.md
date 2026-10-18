# Org.OpenAPITools.Model.CustomerRevenueSystemConfigurationCreateCustomerInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Provider** | **RevenueSystemProviderType** |  | 
**VarConfiguration** | **Dictionary&lt;string, Object&gt;** | Configuration for the revenue system provider. The structure of this object is specific to the revenue system provider. For NetSuite, this should contain &#x60;netsuite_customer_id&#x60;. | [optional] 
**DeliveryMethodId** | **Guid** | ID of the delivery method to use for this customer. If not provided, the &#x60;delivery_method&#x60; must be provided. | [optional] 
**DeliveryMethod** | **RevenueSystemDeliveryMethodType** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


# Org.OpenAPITools.Model.ProService

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | 
**ProductId** | **Guid** |  | 
**UnitPrice** | **decimal** | Unit price for the charge. Will be multiplied by quantity to determine the amount and must be specified. | 
**Quantity** | **decimal** | Quantity for the charge. Will be multiplied by unit_price to determine the amount. | 
**MaxAmount** | **decimal** | Maximum amount for the term. | 
**Description** | **string** |  | [optional] 
**NetsuiteSalesOrderId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


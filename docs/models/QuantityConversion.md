# Org.OpenAPITools.Model.QuantityConversion
Optional. Only valid for USAGE products. If provided, the quantity will be converted using the provided conversion factor and operation. For example, if the operation is \"multiply\" and the conversion factor is 100, then the quantity will be multiplied by 100. This can be used in cases where data is sent in one unit and priced in another.  For example, data could be sent in MB and priced in GB. In this case, the conversion factor would be 1024 and the operation would be \"divide\".

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ConversionFactor** | **decimal** | The factor to multiply or divide the quantity by. | 
**Operation** | **string** | The operation to perform on the quantity | 
**Name** | **string** | Optional name for this conversion. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


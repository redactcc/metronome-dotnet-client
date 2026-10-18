# Org.OpenAPITools.Model.ProductListItemUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **DateTime** |  | 
**CreatedBy** | **string** |  | 
**Name** | **string** |  | [optional] 
**StartingAt** | **DateTime** |  | [optional] 
**IsRefundable** | **bool** |  | [optional] 
**BillableMetricId** | **Guid** |  | [optional] 
**QuantityConversion** | [**QuantityConversion**](QuantityConversion.md) |  | [optional] 
**QuantityRounding** | [**QuantityRounding**](QuantityRounding.md) |  | [optional] 
**NetsuiteInternalItemId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**NetsuiteOverageItemId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**CompositeProductIds** | **List&lt;Guid&gt;** |  | [optional] 
**CompositeTags** | **List&lt;string&gt;** |  | [optional] 
**Tags** | **List&lt;string&gt;** |  | [optional] 
**ExcludeFreeUsage** | **bool** |  | [optional] 
**IncludeCompositeSpend** | **bool** | Only for composite products. If true, allows a composite to incorporate spend from other composite products. Defaults to false | [optional] 
**PricingGroupKey** | **List&lt;string&gt;** | For USAGE products only. If set, pricing for this product will be determined for each pricing_group_key value, as opposed to the product as a whole. The superset of values in the pricing group key and presentation group key must be set as one compound group key on the billable metric. | [optional] 
**PresentationGroupKey** | **List&lt;string&gt;** | For USAGE products only. Groups usage line items on invoices. The superset of values in the pricing group key and presentation group key must be set as one compound group key on the billable metric. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


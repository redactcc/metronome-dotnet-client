# Org.OpenAPITools.Model.CreateProductListItemPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | displayed on invoices | 
**Type** | **string** |  | 
**NetsuiteInternalItemId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**NetsuiteOverageItemId** | **string** | This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**BillableMetricId** | **Guid** | Required for USAGE products | [optional] 
**SqlBreakdownGranularity** | **string** | Defines the breakdown behavior when calculating usage from SQL Billable Metrics. If set to &#39;service_period&#39; (default), the usage will be evaluated once for all events the invoice service period and the usage will be applied at the last instant of the invoice. If set to &#39;hour&#39;, it will be broken down and evaluated for each hour. For most use cases, &#39;hour&#39; is recommended. The setting has no effect for Streaming Billable Metrics. | [optional] 
**CompositeProductIds** | **List&lt;Guid&gt;** | Required for COMPOSITE products | [optional] 
**CompositeTags** | **List&lt;string&gt;** | Required for COMPOSITE products | [optional] 
**IsRefundable** | **bool** | This field&#39;s availability is dependent on your client&#39;s configuration. Defaults to true. | [optional] 
**CompositeScope** | **string** | Determines what spend contributes to calculating this charge. When composite scope is contract, calculates composite charge based on applicable spend per contract. When composite scope is customer, calculates composite charge based on applicable spend across all customer contracts. Defaults to contract. | [optional] 
**ExcludeFreeUsage** | **bool** | Beta feature only available for composite products. If true, products with $0 will not be included when computing composite usage. Defaults to false | [optional] 
**IncludeCompositeSpend** | **bool** | Only for composite products. If true, allows a composite to incorporate spend from other composite products. Defaults to false | [optional] 
**Tags** | **List&lt;string&gt;** |  | [optional] 
**PricingGroupKey** | **List&lt;string&gt;** | For USAGE products only. If set, pricing for this product will be determined for each pricing_group_key value, as opposed to the product as a whole. The superset of values in the pricing group key and presentation group key must be set as one compound group key on the billable metric. | [optional] 
**PresentationGroupKey** | **List&lt;string&gt;** | For USAGE products only. Groups usage line items on invoices. The superset of values in the pricing group key and presentation group key must be set as one compound group key on the billable metric. | [optional] 
**QuantityConversion** | [**QuantityConversion**](QuantityConversion.md) |  | [optional] 
**QuantityRounding** | [**QuantityRounding**](QuantityRounding.md) |  | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


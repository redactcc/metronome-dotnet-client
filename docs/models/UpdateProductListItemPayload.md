# Org.OpenAPITools.Model.UpdateProductListItemPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProductId** | **Guid** | ID of the product to update | 
**StartingAt** | **DateTime** | Timestamp representing when the update should go into effect. It must be on an hour boundary (e.g. 1:00, not 1:30). | 
**Name** | **string** | displayed on invoices. If not provided, defaults to product&#39;s current name. | [optional] 
**IsRefundable** | **bool** | Defaults to product&#39;s current refundability status. This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**ExcludeFreeUsage** | **bool** | Beta feature only available for composite products. If true, products with $0 will not be included when computing composite usage. Defaults to false | [optional] 
**IncludeCompositeSpend** | **bool** | Only for composite products. If true, allows a composite to incorporate spend from other composite products. Defaults to false | [optional] 
**BillableMetricId** | **Guid** | Available for USAGE products only. If not provided, defaults to product&#39;s current billable metric. | [optional] 
**SqlBreakdownGranularity** | **string** | Defines the breakdown behavior when calculating usage from SQL Billable Metrics. If set to &#39;service_period&#39; (default), the usage will be evaluated once for all events the invoice service period and the usage will be applied at the last instant of the invoice. If set to &#39;hour&#39;, it will be broken down and evaluated for each hour. For most use cases, &#39;hour&#39; is recommended. The setting has no effect for Streaming Billable Metrics. | [optional] 
**NetsuiteInternalItemId** | **string** | If not provided, defaults to product&#39;s current netsuite_internal_item_id. This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**NetsuiteOverageItemId** | **string** | Available for USAGE and COMPOSITE products only. If not provided, defaults to product&#39;s current netsuite_overage_item_id. This field&#39;s availability is dependent on your client&#39;s configuration. | [optional] 
**CompositeProductIds** | **List&lt;Guid&gt;** | Available for COMPOSITE products only. If not provided, defaults to product&#39;s current composite_product_ids. | [optional] 
**QuantityConversion** | [**QuantityConversion**](QuantityConversion.md) |  | [optional] 
**QuantityRounding** | [**QuantityRounding**](QuantityRounding.md) |  | [optional] 
**Tags** | **List&lt;string&gt;** | If not provided, defaults to product&#39;s current tags | [optional] 
**CompositeTags** | **List&lt;string&gt;** | Available for COMPOSITE products only. If not provided, defaults to product&#39;s current composite_tags. | [optional] 
**PricingGroupKey** | **List&lt;string&gt;** | For USAGE products only. If set, pricing for this product will be determined for each pricing_group_key value, as opposed to the product as a whole. The superset of values in the pricing group key and presentation group key must be set as one compound group key on the billable metric. | [optional] 
**PresentationGroupKey** | **List&lt;string&gt;** | For USAGE products only. Groups usage line items on invoices. The superset of values in the pricing group key and presentation group key must be set as one compound group key on the billable metric. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


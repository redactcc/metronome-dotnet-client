# Org.OpenAPITools.Model.InvoiceLineItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Total** | **decimal** |  | 
**Type** | **string** | The type of line item.  - &#x60;scheduled&#x60;: Line item is associated with a scheduled charge. View the scheduled_charge_id on the line item. - &#x60;commit_purchase&#x60;: Line item is associated with a payment for a prepaid commit. View the commit_id on the line item. - &#x60;usage&#x60;: Line item is associated with a usage product or composite product. View the product_id on the line item to determine which product. - &#x60;subscription&#x60;: Line item is associated with a subscription. e.g. monthly recurring payment for an in-advance subscription. - &#x60;applied_commit_or_credit&#x60;: On metronome invoices, applied commits and credits are associated with their own line items. These line items have negative totals. Use the applied_commit_or_credit object on the line item to understand the id of the applied commit or credit, and its type. Note that the application of a postpaid commit is associated with a line item, but the total on the line item is not included in the invoice&#39;s total as postpaid commits are paid in-arrears. - &#x60;cpu_conversion&#x60;: Line item converting between a custom pricing unit and fiat currency, using the conversion rate set on the rate card. This line item will appear when there are products priced in custom pricing units, and there is insufficient prepaid commit/credit in that custom pricing unit to fully cover the spend. Then, the outstanding spend in custom pricing units will be converted to fiat currency using a cpu_conversion line item.  | 
**CreditType** | [**CreditType**](CreditType.md) |  | 
**Quantity** | **decimal** | The quantity associated with the line item. | [optional] 
**UnitPrice** | **decimal** | The unit price associated with the line item. | [optional] 
**ListPrice** | [**Rate**](Rate.md) |  | [optional] 
**ProductId** | **Guid** | ID of the product associated with the line item. | [optional] 
**ProductCustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**ProductTags** | **List&lt;string&gt;** |  | [optional] 
**ProductType** | **string** | The type of the line item&#39;s product. Possible values are &#x60;FixedProductListItem&#x60; (for &#x60;FIXED&#x60; type products), &#x60;UsageProductListItem&#x60; (for &#x60;USAGE&#x60; type products), &#x60;SubscriptionProductListItem&#x60; (for &#x60;SUBSCRIPTION&#x60; type products) or &#x60;CompositeProductListItem&#x60; (for &#x60;COMPOSITE&#x60; type products).  For scheduled charges, commit and credit payments, the value is &#x60;FixedProductListItem&#x60;.  | [optional] 
**NetsuiteItemId** | **string** |  | [optional] 
**IsProrated** | **bool** | Indicates whether the line item is prorated for &#x60;SUBSCRIPTION&#x60; type product. | [optional] 
**StartingAt** | **DateTime** | The line item&#39;s start date (inclusive). | [optional] 
**EndingBefore** | **DateTime** | The line item&#39;s end date (exclusive). | [optional] 
**CommitId** | **Guid** | For line items with product of &#x60;USAGE&#x60;, &#x60;SUBSCRIPTION&#x60;, &#x60;COMPOSITE&#x60;, or &#x60;CPU_CONVERSION&#x60; types, the ID of the credit or commit that was applied to this line item. For line items with product type of &#x60;FIXED&#x60;, the ID of the prepaid or postpaid commit that is being paid for. | [optional] 
**AppliedCommitOrCredit** | [**AppliedCommitOrCredit**](AppliedCommitOrCredit.md) |  | [optional] 
**CommitCustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**CommitSegmentId** | **Guid** |  | [optional] 
**CommitType** | **string** | &#x60;PrepaidCommit&#x60; (for commit types &#x60;PREPAID&#x60; and &#x60;CREDIT&#x60;) or &#x60;PostpaidCommit&#x60; (for commit type &#x60;POSTPAID&#x60;). | [optional] 
**CommitNetsuiteSalesOrderId** | **string** |  | [optional] 
**CommitNetsuiteItemId** | **string** |  | [optional] 
**PostpaidCommit** | [**PostpaidCommit**](PostpaidCommit.md) |  | [optional] 
**ResellerType** | **ResellerType** |  | [optional] 
**CustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**PricingGroupValues** | **Dictionary&lt;string, string&gt;** | Includes the pricing group values associated with this line item if dimensional pricing is used. | [optional] 
**PresentationGroupValues** | **Dictionary&lt;string, string&gt;** | Includes the presentation group values associated with this line item if presentation group keys are used. | [optional] 
**Metadata** | **string** |  | [optional] 
**NetsuiteInvoiceBillingStart** | **DateTime** | The start date for the billing period on the invoice. | [optional] 
**NetsuiteInvoiceBillingEnd** | **DateTime** | The end date for the billing period on the invoice. | [optional] 
**ProfessionalServiceId** | **Guid** |  | [optional] 
**ProfessionalServiceCustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**ScheduledChargeId** | **Guid** | ID of scheduled charge. | [optional] 
**ScheduledChargeCustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**SubscriptionCustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**SubscriptionId** | **Guid** | ID of the subscription that this line item is associated with. Only present on line items with product of &#x60;SUBSCRIPTION&#x60; type. | [optional] 
**Tier** | [**TierMetadata**](TierMetadata.md) |  | [optional] 
**DiscountId** | **Guid** | ID of the discount applied to this line item. | [optional] 
**DiscountCustomFields** | **Dictionary&lt;string, string&gt;** | Custom fields to be added eg. { \&quot;key1\&quot;: \&quot;value1\&quot;, \&quot;key2\&quot;: \&quot;value2\&quot; } | [optional] 
**Origin** | [**InvoiceLineItemOrigin**](InvoiceLineItemOrigin.md) |  | [optional] 
**QuantityConsumed** | **decimal** | Present on applied commit line items for quantity-based commits. Represents the unit quantity deducted the commit. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


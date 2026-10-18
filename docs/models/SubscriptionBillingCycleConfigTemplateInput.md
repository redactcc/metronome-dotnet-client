# Org.OpenAPITools.Model.SubscriptionBillingCycleConfigTemplateInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**InvoicePlacement** | **string** | Controls whether subscriptions consolidate onto usage invoices. Defaults to ON_USAGE_INVOICE if omitted. | [optional] 
**BillingCycleAnchor** | **string** | Controls which date each subscription materialized from this template anchors its billing cycle to. CUSTOM_DATE requires a subscription_anchor_date supplied per contract via package customizations. Defaults to USAGE_STATEMENT_ANCHOR (the contract&#39;s usage statement anchor) if omitted. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


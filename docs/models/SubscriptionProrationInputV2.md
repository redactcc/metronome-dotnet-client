# Org.OpenAPITools.Model.SubscriptionProrationInputV2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**IsProrated** | **bool** | Indicates if the partial period will be prorated or charged a full amount. | [optional] 
**InvoiceBehavior** | **string** | Indicates how mid-period quantity adjustments are invoiced. **BILL_IMMEDIATELY**: Only available when collection schedule is &#x60;ADVANCE&#x60;. The quantity increase will be billed immediately on the scheduled date. **BILL_ON_NEXT_COLLECTION_DATE**: The quantity increase will be billed for in-arrears at the end of the period.  | [optional] 
**Rounding** | [**ProrationRoundingConfigV2**](ProrationRoundingConfigV2.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


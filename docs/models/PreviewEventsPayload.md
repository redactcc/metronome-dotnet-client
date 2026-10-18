# Org.OpenAPITools.Model.PreviewEventsPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Events** | [**List&lt;PreviewEvent&gt;**](PreviewEvent.md) | Array of usage events to include in the preview calculation. Must contain at least one event in &#x60;merge&#x60; mode.  | 
**Mode** | **string** | Controls how the provided events are combined with existing usage data. Use &#x60;replace&#x60; to calculate the preview as if these are the only events for the customer, ignoring all historical usage.  Use &#x60;merge&#x60; to combine these events with the customer&#39;s existing usage.  Defaults to &#x60;replace&#x60;.  | [optional] [default to ModeEnum.Replace]
**SkipZeroQtyLineItems** | **bool** | When &#x60;true&#x60;, line items with zero quantity are excluded from the response. | [optional] [default to false]

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


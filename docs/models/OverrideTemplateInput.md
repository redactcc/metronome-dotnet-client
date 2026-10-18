# Org.OpenAPITools.Model.OverrideTemplateInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StartingAtOffset** | [**RelativeDate**](RelativeDate.md) |  | 
**OverrideSpecifiers** | [**List&lt;OverrideSpecifierInput&gt;**](OverrideSpecifierInput.md) | Specifies which products the override will apply to. | 
**Duration** | [**RelativeDate**](RelativeDate.md) |  | [optional] 
**Entitled** | **bool** |  | [optional] 
**Type** | **string** | Overwrites are prioritized over multipliers and tiered overrides. | [optional] 
**Multiplier** | **decimal** | Required for MULTIPLIER type. Must be &gt;&#x3D;0. | [optional] 
**Priority** | **decimal** | Required for EXPLICIT multiplier prioritization scheme and all TIERED overrides. Under EXPLICIT prioritization, overwrites are prioritized first, and then tiered and multiplier overrides are prioritized by their priority value (lowest first). Must be &gt; 0. | [optional] 
**OverwriteRate** | [**OverwriteRateInput**](OverwriteRateInput.md) |  | [optional] 
**Tiers** | [**List&lt;OverrideTierInput&gt;**](OverrideTierInput.md) | Required for TIERED type. Must have at least one tier. | [optional] 
**IsCommitSpecific** | **bool** | Indicates whether the override should only apply to commits. Defaults to &#x60;false&#x60;. If &#x60;true&#x60; you can specify relevant commits in &#x60;override_specifiers&#x60; by passing &#x60;commit_ids&#x60;, &#x60;recurring_commit_ids&#x60;, or &#x60;any_commit_or_credit_ids&#x60;.  If you do not specify any of these fields, the override will apply when consuming any prepaid commit, postpaid commit, or credit | [optional] 
**Target** | **string** | Indicates whether the override applies to commit rates or list rates. Can only be used for overrides that have &#x60;is_commit_specific&#x60; set to &#x60;true&#x60;. Defaults to &#x60;\&quot;LIST_RATE\&quot;&#x60;. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


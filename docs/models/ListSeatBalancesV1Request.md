# Org.OpenAPITools.Model.ListSeatBalancesV1Request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **Guid** | The customer ID to retrieve seat balances for | 
**ContractId** | **Guid** | The contract ID to retrieve seat balances for | 
**SubscriptionIds** | **List&lt;Guid&gt;** | Optional filter to only include seats from specific subscriptions. If subscriptions ids are not mapped to SEAT_BASED subscriptions, error will be returned. | [optional] 
**SeatIds** | **List&lt;string&gt;** | Optional filter to only include specific seats. | [optional] 
**SkipMissingSeatIds** | **bool** | When true, any seat_ids not found in contract subscriptions will be silently omitted from the response instead of returning a 400 error. | [optional] [default to false]
**IncludeCreditsAndCommits** | **bool** | Include credits and commits in the response | [optional] [default to false]
**IncludeLedgers** | **bool** | Include ledger entries for each commit and commit. &#x60;include_credits_and_commits&#x60; must be set to &#x60;true&#x60; for &#x60;include_ledgers&#x3D;true&#x60; to apply. | [optional] [default to false]
**StartingAt** | **DateTime** | Include only commits or credits with access effective on or after this date (cannot be used with covering_date). | [optional] 
**EffectiveBefore** | **DateTime** | Include only commits or credits with access effective on or before this date (cannot be used with covering_date). | [optional] 
**CoveringDate** | **DateTime** | Include only commits or credits with access that cover this specific date (cannot be used with starting_at or ending_before). | [optional] 
**Limit** | **int** | Maximum number of seats to return. Range: 1-100. Default: 25. When &#x60;include_credits_and_commits &#x3D; true&#x60;, if the total commits/credits across all seats exceeds 100, a limit of 100 applies to the total credits and commits. Seats are included greedily to maximize the number of seats returned. Example: if seat 1 has 98 commits and seat 2 has 10 commits, both seats will be returned (total: 108 commits). Each returned seat includes all of its associated credits and commits.  | [optional] 
**Cursor** | **string** | Page token from a previous response to retrieve the next page | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


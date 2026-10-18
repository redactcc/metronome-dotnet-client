# Org.OpenAPITools.Model.CreditGrantRolloverSettings
Configure a rollover for this credit grant so if it expires it rolls over a configured amount to a new credit grant. This feature is currently opt-in only. Contact Metronome to be added to the beta.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ExpiresAt** | **DateTime** | The date to expire the rollover credits. | 
**Priority** | **decimal** | The priority to give the rollover credit grant that gets created when a rollover happens. | 
**RolloverAmount** | [**CreditGrantRolloverSettingsRolloverAmount**](CreditGrantRolloverSettingsRolloverAmount.md) |  | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


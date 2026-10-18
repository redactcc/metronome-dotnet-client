# Org.OpenAPITools.Model.BaseThresholdCommit

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProductId** | **string** | The commit product that will be used to generate the line item for commit payment. | 
**Name** | **string** | Specify the name of the line item for the threshold charge. If left blank, it will default to the commit product name. | [optional] 
**Description** | **string** |  | [optional] 
**Priority** | **decimal** | The priority of the commit, used to determine drawdown order. Lower priority commits are consumed first. Defaults to 100 if not specified. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


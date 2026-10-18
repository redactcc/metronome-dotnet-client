# Org.OpenAPITools.Api.CustomFieldsApi

All URIs are relative to *https://api.metronome.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddCustomFieldKeyV1**](CustomFieldsApi.md#addcustomfieldkeyv1) | **POST** /v1/customFields/addKey | Create a custom field key |
| [**DeleteCustomFieldsV1**](CustomFieldsApi.md#deletecustomfieldsv1) | **POST** /v1/customFields/deleteValues | Delete custom fields |
| [**DisableCustomFieldKeyV1**](CustomFieldsApi.md#disablecustomfieldkeyv1) | **POST** /v1/customFields/removeKey | Delete a custom field key |
| [**ListCustomFieldKeysV1**](CustomFieldsApi.md#listcustomfieldkeysv1) | **POST** /v1/customFields/listKeys | List custom field keys |
| [**SetCustomFieldsV1**](CustomFieldsApi.md#setcustomfieldsv1) | **POST** /v1/customFields/setValues | Set custom field values |

<a id="addcustomfieldkeyv1"></a>
# **AddCustomFieldKeyV1**
> void AddCustomFieldKeyV1 (AddCustomFieldKeyV1Request addCustomFieldKeyV1Request = null)

Create a custom field key

Creates a new custom field key for a given entity (e.g. billable metric, contract, alert).  Custom fields are properties that you can add to Metronome objects to store metadata like foreign keys or other descriptors. This metadata can get transferred to or accessed by other systems to contextualize Metronome data and power business processes. For example, to service workflows like revenue recognition, reconciliation, and invoicing, custom fields help Metronome know the relationship between entities in the platform and third-party systems.  ### Use this endpoint to: - Create a new custom field key for Customer objects in Metronome. You can then use the Set Custom Field Values endpoint to set the value of this key for a specific customer.  - Specify whether the key should enforce uniqueness. If the key is set to enforce uniqueness and you attempt to set a custom field value for the key that already exists, it will fail.   ### Usage guidelines: - Custom fields set on commits, credits, and contracts can be used to scope alert evaluation. For example, you can create a spend threshold alert that only considers spend associated with contracts with custom field key `contract_type` and value `paygo` - Custom fields set on products can be used in the Stripe integration to set metadata on invoices. - Custom fields for customers, contracts, invoices, products, commits, scheduled charges, and subscriptions are passed down to the invoice. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **addCustomFieldKeyV1Request** | [**AddCustomFieldKeyV1Request**](AddCustomFieldKeyV1Request.md) | Add a key to the allow list for an entity | [optional]  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletecustomfieldsv1"></a>
# **DeleteCustomFieldsV1**
> void DeleteCustomFieldsV1 (DeleteCustomFieldsV1Request deleteCustomFieldsV1Request = null)

Delete custom fields

Remove specific custom field values from a Metronome entity instance by specifying the field keys to delete. Use this endpoint to clean up unwanted custom field data while preserving other fields on the same entity. Requires the entity type, entity ID, and array of keys to remove. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deleteCustomFieldsV1Request** | [**DeleteCustomFieldsV1Request**](DeleteCustomFieldsV1Request.md) | Delete one or more custom fields | [optional]  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="disablecustomfieldkeyv1"></a>
# **DisableCustomFieldKeyV1**
> void DisableCustomFieldKeyV1 (DisableCustomFieldKeyV1Request disableCustomFieldKeyV1Request = null)

Delete a custom field key

Removes a custom field key from the allowlist for a specific entity type, preventing future use of that key across all instances of the entity. Existing values for this key on entity instances will no longer be accessible once the key is removed. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **disableCustomFieldKeyV1Request** | [**DisableCustomFieldKeyV1Request**](DisableCustomFieldKeyV1Request.md) | Remove a key from the allow list for an entity | [optional]  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listcustomfieldkeysv1"></a>
# **ListCustomFieldKeysV1**
> ListCustomFieldKeysV1200Response ListCustomFieldKeysV1 (string nextPage = null, ListCustomFieldKeysV1Request listCustomFieldKeysV1Request = null)

List custom field keys

Retrieve all your active custom field keys, with optional filtering by entity type (customer, contract, product, etc.). Use this endpoint to discover what custom field keys are available before setting values on entities or to audit your custom field configuration across different entity types. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **nextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional]  |
| **listCustomFieldKeysV1Request** | [**ListCustomFieldKeysV1Request**](ListCustomFieldKeysV1Request.md) |  | [optional]  |

### Return type

[**ListCustomFieldKeysV1200Response**](ListCustomFieldKeysV1200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="setcustomfieldsv1"></a>
# **SetCustomFieldsV1**
> void SetCustomFieldsV1 (SetCustomFieldsV1Request setCustomFieldsV1Request = null)

Set custom field values

Sets custom field values on a specific Metronome entity instance. Overwrites existing values for matching keys while preserving other fields. All updates are transactional—either all values are set or none are. Custom field values are limited to 200 characters each.  Adding or updating custom fields on credits, commits, or contracts does not emit `credit.edit`, `commit.edit`, or `contract.edit` events. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **setCustomFieldsV1Request** | [**SetCustomFieldsV1Request**](SetCustomFieldsV1Request.md) | The custom field values to set | [optional]  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


# Org.OpenAPITools.Api.ProductsApi

All URIs are relative to *https://api.metronome.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveProductListItemV1**](ProductsApi.md#archiveproductlistitemv1) | **POST** /v1/contract-pricing/products/archive | Archive a product |
| [**CreateProductV1**](ProductsApi.md#createproductv1) | **POST** /v1/contract-pricing/products/create | Create a product |
| [**GetProductV1**](ProductsApi.md#getproductv1) | **POST** /v1/contract-pricing/products/get | Get a product |
| [**ListProductsV1**](ProductsApi.md#listproductsv1) | **POST** /v1/contract-pricing/products/list | List products |
| [**UpdateProductV1**](ProductsApi.md#updateproductv1) | **POST** /v1/contract-pricing/products/update | Update a product |

<a id="archiveproductlistitemv1"></a>
# **ArchiveProductListItemV1**
> ArchiveAlertV1200Response ArchiveProductListItemV1 (ArchiveProductListItemPayload archiveProductListItemPayload = null)

Archive a product

Archive a product. Any current rate cards associated with this product will continue to function as normal. However, it will no longer be available as an option for newly created rates. Once you archive a product, you can still retrieve it in the UI and API, but you cannot unarchive it. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **archiveProductListItemPayload** | [**ArchiveProductListItemPayload**](ArchiveProductListItemPayload.md) | Archive a product | [optional]  |

### Return type

[**ArchiveAlertV1200Response**](ArchiveAlertV1200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Bad request |  -  |
| **404** | The specified resource was not found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createproductv1"></a>
# **CreateProductV1**
> ArchiveAlertV1200Response CreateProductV1 (CreateProductListItemPayload createProductListItemPayload = null)

Create a product

Create a new product object. Products in Metronome represent your company's individual product or service offerings. A Product can be thought of as the basic unit of a line item on the invoice. This is analogous to SKUs or items in an ERP system. Give the product a meaningful name as they will appear on customer invoices. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createProductListItemPayload** | [**CreateProductListItemPayload**](CreateProductListItemPayload.md) | Create a new product | [optional]  |

### Return type

[**ArchiveAlertV1200Response**](ArchiveAlertV1200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getproductv1"></a>
# **GetProductV1**
> GetProductV1200Response GetProductV1 (Id id = null)

Get a product

Retrieve a product by its ID, including all metadata and historical changes. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | [**Id**](Id.md) | The ID of the product to get | [optional]  |

### Return type

[**GetProductV1200Response**](GetProductV1200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | The specified resource was not found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listproductsv1"></a>
# **ListProductsV1**
> ListProductsV1200Response ListProductsV1 (int limit = null, string nextPage = null, ListProductsPayload listProductsPayload = null)

List products

Get a paginated list of all products in your organization with their complete configuration, version history, and metadata. By default excludes archived products unless explicitly requested via the `archive_filter` parameter. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int** | Max number of results that should be returned | [optional]  |
| **nextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional]  |
| **listProductsPayload** | [**ListProductsPayload**](ListProductsPayload.md) | Get list of products | [optional]  |

### Return type

[**ListProductsV1200Response**](ListProductsV1200Response.md)

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

<a id="updateproductv1"></a>
# **UpdateProductV1**
> ArchiveAlertV1200Response UpdateProductV1 (UpdateProductListItemPayload updateProductListItemPayload = null)

Update a product

Updates a product's configuration while maintaining billing continuity for active customers. Use this endpoint to modify product names, metrics, pricing rules, and composite settings without disrupting ongoing billing cycles. Changes are scheduled using the starting_at timestamp, which must be on an hour boundary—set future dates to schedule updates ahead of time, or past dates for retroactive changes. Returns the updated product ID upon success.   ### Usage guidance:  - Product type cannot be changed after creation. For incorrect product types, create a new product and archive the original instead. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateProductListItemPayload** | [**UpdateProductListItemPayload**](UpdateProductListItemPayload.md) | Updates a product&#39;s configuration while maintaining billing continuity for active customers. Use this endpoint to modify product names, metrics, pricing rules, and composite settings without disrupting ongoing billing cycles. Changes are scheduled using the starting_at timestamp, which must be on an hour boundary–set future dates to schedule updates ahead of time, or past dates for retroactive changes. Returns the updated product ID upon success.   Usage guidance:  Product type cannot be changed after creation. For incorrect product types, create a new product and archive the original instead.  | [optional]  |

### Return type

[**ArchiveAlertV1200Response**](ArchiveAlertV1200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Bad request |  -  |
| **404** | The specified resource was not found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


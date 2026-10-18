# Org.OpenAPITools.Api.BillableMetricsApi

All URIs are relative to *https://api.metronome.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveBillableMetricV1**](BillableMetricsApi.md#archivebillablemetricv1) | **POST** /v1/billable-metrics/archive | Archive a billable metric |
| [**CreateBillableMetricV1V1**](BillableMetricsApi.md#createbillablemetricv1v1) | **POST** /v1/billable-metrics/create | Create a billable metric |
| [**GetBillableMetricV1**](BillableMetricsApi.md#getbillablemetricv1) | **GET** /v1/billable-metrics/{billable_metric_id} | Get a billable metric |
| [**ListAllBillableMetricsV1**](BillableMetricsApi.md#listallbillablemetricsv1) | **GET** /v1/billable-metrics | List all billable metrics |
| [**ListBillableMetricsV1**](BillableMetricsApi.md#listbillablemetricsv1) | **GET** /v1/customers/{customer_id}/billable-metrics | Get billable metrics for a customer |
| [**UpdateBillableMetricV1**](BillableMetricsApi.md#updatebillablemetricv1) | **PUT** /v1/billable-metrics/{billable_metric_id} | Update a billable metric |

<a id="archivebillablemetricv1"></a>
# **ArchiveBillableMetricV1**
> ArchiveAlertV1200Response ArchiveBillableMetricV1 (Id id = null)

Archive a billable metric

Use this endpoint to retire billable metrics that are no longer used. After a billable metric is archived, that billable metric can no longer be used in any new Products to define how that product should be metered. If you archive a billable metric that is already associated with a Product, the Product will continue to function as usual, metering based on the definition of the archived billable metric.   Archived billable metrics will be returned on the `getBillableMetric` and `listBillableMetrics` endpoints with a populated `archived_at` field. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | [**Id**](Id.md) | The ID of the billable metric to archive | [optional]  |

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
| **404** | The specified resource was not found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createbillablemetricv1v1"></a>
# **CreateBillableMetricV1V1**
> ArchiveAlertV1200Response CreateBillableMetricV1V1 (CreateBillableMetricV1Payload createBillableMetricV1Payload = null)

Create a billable metric

Create billable metrics programmatically with this endpoint—an essential step in configuring your pricing and packaging in Metronome.  A billable metric is a customizable query that filters and aggregates events from your event stream. These metrics are continuously tracked as usage data enters Metronome through the ingestion pipeline. The ingestion process transforms raw usage data into actionable pricing metrics, enabling accurate metering and billing for your products.  ### Use this endpoint to:  - Create individual or multiple billable metrics as part of a setup workflow. - Automate the entire pricing configuration process, from metric creation to customer contract setup. - Define metrics using either standard filtering/aggregation or a custom SQL query.  ### Key response fields:  - The ID of the billable metric that was created - The created billable metric will be available to be used in Products, usage endpoints, and alerts.   ### Usage guidelines:  - Metrics defined using standard filtering and aggregation are Streaming billable metrics, which have been optimized for ultra low latency and high throughput workflows.  - Use SQL billable metrics if you require more flexible aggregation options. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createBillableMetricV1Payload** | [**CreateBillableMetricV1Payload**](CreateBillableMetricV1Payload.md) | The details of the billable metric to create. | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getbillablemetricv1"></a>
# **GetBillableMetricV1**
> GetBillableMetricV1200Response GetBillableMetricV1 (Guid billableMetricId)

Get a billable metric

Retrieves the complete configuration for a specific billable metric by its ID. Use this to review billable metric setup before associating it with products. Returns the metric's `name`, `event_type_filter`, `property_filters`, `aggregation_type`, `aggregation_key`, `group_keys`, `custom fields`, and `SQL query` (if it's a SQL billable metric).   Important:  - Archived billable metrics will include an `archived_at` timestamp; they no longer process new usage events but remain accessible for historical reference. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **billableMetricId** | **Guid** |  |  |

### Return type

[**GetBillableMetricV1200Response**](GetBillableMetricV1200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | The specified resource was not found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listallbillablemetricsv1"></a>
# **ListAllBillableMetricsV1**
> ListAllBillableMetricsV1200Response ListAllBillableMetricsV1 (int limit = null, string nextPage = null, bool includeArchived = null)

List all billable metrics

Retrieves all billable metrics with their complete configurations. Use this for programmatic discovery and management of billable metrics, such as associating metrics to products and auditing for orphaned or archived metrics.  Important: Archived metrics are excluded by default; use `include_archived`=`true` parameter to include them. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int** | Max number of results that should be returned | [optional]  |
| **nextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional]  |
| **includeArchived** | **bool** | If true, the list of returned metrics will include archived metrics | [optional]  |

### Return type

[**ListAllBillableMetricsV1200Response**](ListAllBillableMetricsV1200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listbillablemetricsv1"></a>
# **ListBillableMetricsV1**
> ListBillableMetricsV1200Response ListBillableMetricsV1 (Guid customerId, int limit = null, string nextPage = null, bool onCurrentPlan = null, bool includeArchived = null)

Get billable metrics for a customer

Get all billable metrics available for a specific customer. Supports pagination and filtering by current plan status or archived metrics. Use this endpoint to see which metrics are being tracked for billing calculations for a given customer. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **Guid** |  |  |
| **limit** | **int** | Max number of results that should be returned | [optional]  |
| **nextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional]  |
| **onCurrentPlan** | **bool** | If true, the list of metrics will be filtered to just ones that are on the customer&#39;s current plan | [optional]  |
| **includeArchived** | **bool** | If true, the list of returned metrics will include archived metrics | [optional]  |

### Return type

[**ListBillableMetricsV1200Response**](ListBillableMetricsV1200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatebillablemetricv1"></a>
# **UpdateBillableMetricV1**
> ArchiveAlertV1200Response UpdateBillableMetricV1 (Guid billableMetricId, UpdateBillableMetricV1Request updateBillableMetricV1Request = null)

Update a billable metric

Updates only the display name of an existing billable metric. Use this to correct mistakes or apply standardized naming conventions across all billable metrics. Returns the billable metric ID to confirm the update.   Important: Only the name can be modified via this endpoint; configurations cannot be changed after creation.   #### Example workflow: If you need to make changes to a streaming billable metric, for example, Metronome supports easily rolling out these changes using a simple workflow: 1. Duplicate the billable metric 2. Make required changes 3. Save the metric 4. Navigate to the product you have associated with the incorrect metric 5. Schedule the product to reference the newly created metric on the appropriate date 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **billableMetricId** | **Guid** |  |  |
| **updateBillableMetricV1Request** | [**UpdateBillableMetricV1Request**](UpdateBillableMetricV1Request.md) | The billable metric to update | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


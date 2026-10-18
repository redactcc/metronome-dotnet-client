# Org.OpenAPITools.Api.ApprovalRequestsApi

All URIs are relative to *https://api.metronome.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ApproveApprovalRequestV1**](ApprovalRequestsApi.md#approveapprovalrequestv1) | **POST** /v1/approval_requests/{id}/approve | Approve a pending approval request |
| [**DenyApprovalRequestV1**](ApprovalRequestsApi.md#denyapprovalrequestv1) | **POST** /v1/approval_requests/{id}/deny | Deny a pending approval request |
| [**GetApprovalRequestV1**](ApprovalRequestsApi.md#getapprovalrequestv1) | **GET** /v1/approval_requests/{id} | Get an approval request |
| [**ListApprovalRequestsV1**](ApprovalRequestsApi.md#listapprovalrequestsv1) | **GET** /v1/approval_requests | List approval requests |
| [**SubmitApprovalRequestsV1**](ApprovalRequestsApi.md#submitapprovalrequestsv1) | **POST** /v1/approval_requests | Submit a write operation for human approval |

<a id="approveapprovalrequestv1"></a>
# **ApproveApprovalRequestV1**
> SubmitApprovalRequestsV1200Response ApproveApprovalRequestV1 (Guid id)

Approve a pending approval request

Approves a pending approval request, allowing the queued operation to proceed.  Once approved, the original write operation will be executed automatically and the approval request status will transition to reflect the execution result. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** | The ID of the approval request to approve. |  |

### Return type

[**SubmitApprovalRequestsV1200Response**](SubmitApprovalRequestsV1200Response.md)

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

<a id="denyapprovalrequestv1"></a>
# **DenyApprovalRequestV1**
> SubmitApprovalRequestsV1200Response DenyApprovalRequestV1 (Guid id)

Deny a pending approval request

Denies a pending approval request, preventing the queued operation from executing.  Once denied, the approval request is closed and the original write operation will not be performed. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** | The ID of the approval request to deny. |  |

### Return type

[**SubmitApprovalRequestsV1200Response**](SubmitApprovalRequestsV1200Response.md)

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

<a id="getapprovalrequestv1"></a>
# **GetApprovalRequestV1**
> SubmitApprovalRequestsV1200Response GetApprovalRequestV1 (Guid id)

Get an approval request

Retrieves the details of a single approval request by its ID. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** | The ID of the approval request to retrieve. |  |

### Return type

[**SubmitApprovalRequestsV1200Response**](SubmitApprovalRequestsV1200Response.md)

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

<a id="listapprovalrequestsv1"></a>
# **ListApprovalRequestsV1**
> ListApprovalRequestsV1200Response ListApprovalRequestsV1 (string status = null, int limit = null, string nextPage = null, DateTime createdBefore = null, DateTime createdAfter = null)

List approval requests

Lists all approval requests submitted by agentic tokens for your account. Returns request details including status, token name, approval URL, and the original request payload. Use status and date filters to narrow results. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **status** | **string** | Filter by approval request status. | [optional]  |
| **limit** | **int** | Number of items to return per page. Defaults to 20. | [optional]  |
| **nextPage** | **string** | Cursor for pagination. Use the value from the previous response&#39;s next_page field. | [optional]  |
| **createdBefore** | **DateTime** | Filter to requests created before this timestamp (exclusive). | [optional]  |
| **createdAfter** | **DateTime** | Filter to requests created on or after this timestamp (inclusive). | [optional]  |

### Return type

[**ListApprovalRequestsV1200Response**](ListApprovalRequestsV1200Response.md)

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

<a id="submitapprovalrequestsv1"></a>
# **SubmitApprovalRequestsV1**
> SubmitApprovalRequestsV1200Response SubmitApprovalRequestsV1 (SubmitApprovalRequestsV1Request submitApprovalRequestsV1Request)

Submit a write operation for human approval

Queues a write operation for human review when an agentic token is in use.  When an agent attempts a write operation (e.g. `POST /v1/contracts/create`) using an agentic token, the server returns a `403 AgenticMutationBlocked` error with a pointer to this endpoint. The agent should then call this endpoint with the original request details so a human can review and approve the action.  On success, a pending approval request is created and the response includes an `approval_url` linking to the Approval Dashboard where a human can review, approve, or reject the request. Once approved, the original operation is executed automatically and the dashboard reflects the completed status.  Agents should surface the `approval_url` to the human user (e.g. via chat message or UI link) so they can navigate directly to the approval dashboard to review the request. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **submitApprovalRequestsV1Request** | [**SubmitApprovalRequestsV1Request**](SubmitApprovalRequestsV1Request.md) |  |  |

### Return type

[**SubmitApprovalRequestsV1200Response**](SubmitApprovalRequestsV1200Response.md)

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


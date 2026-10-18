# Org.OpenAPITools.Api.NamedSchedulesApi

All URIs are relative to *https://api.metronome.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetContractNamedScheduleV1**](NamedSchedulesApi.md#getcontractnamedschedulev1) | **POST** /v1/contracts/getNamedSchedule | Get a contract&#39;s named schedule |
| [**GetCustomerNamedScheduleV1**](NamedSchedulesApi.md#getcustomernamedschedulev1) | **POST** /v1/customers/getNamedSchedule | Get a customer&#39;s named schedule |
| [**GetRateCardNamedScheduleV1**](NamedSchedulesApi.md#getratecardnamedschedulev1) | **POST** /v1/contract-pricing/rate-cards/getNamedSchedule | Get a rate card&#39;s named schedule |
| [**ListContractsNamedSchedulesV1**](NamedSchedulesApi.md#listcontractsnamedschedulesv1) | **POST** /v1/contracts/listNamedSchedules | List contract named schedules |
| [**UpdateContractNamedScheduleV1**](NamedSchedulesApi.md#updatecontractnamedschedulev1) | **POST** /v1/contracts/updateNamedSchedule | Update a contract&#39;s named schedule |
| [**UpdateCustomerNamedScheduleV1**](NamedSchedulesApi.md#updatecustomernamedschedulev1) | **POST** /v1/customers/updateNamedSchedule | Update a customer&#39;s named schedule |
| [**UpdateRateCardNamedScheduleV1**](NamedSchedulesApi.md#updateratecardnamedschedulev1) | **POST** /v1/contract-pricing/rate-cards/updateNamedSchedule | Update a rate card&#39;s named schedule |

<a id="getcontractnamedschedulev1"></a>
# **GetContractNamedScheduleV1**
> NamedSchedule GetContractNamedScheduleV1 (GetContractNamedSchedulePayload getContractNamedSchedulePayload = null)

Get a contract's named schedule

Get a named schedule for the given contract. This endpoint's availability is dependent on your client's configuration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **getContractNamedSchedulePayload** | [**GetContractNamedSchedulePayload**](GetContractNamedSchedulePayload.md) | Which customer, contract, schedule name, and date to retrieve. | [optional]  |

### Return type

[**NamedSchedule**](NamedSchedule.md)

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

<a id="getcustomernamedschedulev1"></a>
# **GetCustomerNamedScheduleV1**
> NamedSchedule GetCustomerNamedScheduleV1 (GetCustomerNamedSchedulePayload getCustomerNamedSchedulePayload = null)

Get a customer's named schedule

Get a named schedule for the given customer. This endpoint's availability is dependent on your client's configuration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **getCustomerNamedSchedulePayload** | [**GetCustomerNamedSchedulePayload**](GetCustomerNamedSchedulePayload.md) | Which customer, schedule name, and date to retrieve. | [optional]  |

### Return type

[**NamedSchedule**](NamedSchedule.md)

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

<a id="getratecardnamedschedulev1"></a>
# **GetRateCardNamedScheduleV1**
> NamedSchedule GetRateCardNamedScheduleV1 (GetRateCardNamedSchedulePayload getRateCardNamedSchedulePayload = null)

Get a rate card's named schedule

Get a named schedule for the given rate card. This endpoint's availability is dependent on your client's configuration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **getRateCardNamedSchedulePayload** | [**GetRateCardNamedSchedulePayload**](GetRateCardNamedSchedulePayload.md) | Which rate card, schedule name, and date to retrieve. | [optional]  |

### Return type

[**NamedSchedule**](NamedSchedule.md)

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

<a id="listcontractsnamedschedulesv1"></a>
# **ListContractsNamedSchedulesV1**
> ListContractsNamedSchedulesPage ListContractsNamedSchedulesV1 (ListContractsNamedSchedulesPayload listContractsNamedSchedulesPayload = null)

List contract named schedules

List contract-level named schedules for a customer, optionally scoped to a single contract.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listContractsNamedSchedulesPayload** | [**ListContractsNamedSchedulesPayload**](ListContractsNamedSchedulesPayload.md) | Specify which customer and optional filters to use when listing contract named schedules. | [optional]  |

### Return type

[**ListContractsNamedSchedulesPage**](ListContractsNamedSchedulesPage.md)

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

<a id="updatecontractnamedschedulev1"></a>
# **UpdateContractNamedScheduleV1**
> void UpdateContractNamedScheduleV1 (UpdateContractNamedSchedulePayload updateContractNamedSchedulePayload = null)

Update a contract's named schedule

Update a named schedule for the given contract. This endpoint's availability is dependent on your client's configuration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateContractNamedSchedulePayload** | [**UpdateContractNamedSchedulePayload**](UpdateContractNamedSchedulePayload.md) | The customer, contract, schedule name, date range, and value to set. | [optional]  |

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

<a id="updatecustomernamedschedulev1"></a>
# **UpdateCustomerNamedScheduleV1**
> void UpdateCustomerNamedScheduleV1 (UpdateCustomerNamedSchedulePayload updateCustomerNamedSchedulePayload = null)

Update a customer's named schedule

Update a named schedule for the given customer. This endpoint's availability is dependent on your client's configuration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateCustomerNamedSchedulePayload** | [**UpdateCustomerNamedSchedulePayload**](UpdateCustomerNamedSchedulePayload.md) | The customer, schedule name, date range, and value to set. | [optional]  |

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

<a id="updateratecardnamedschedulev1"></a>
# **UpdateRateCardNamedScheduleV1**
> void UpdateRateCardNamedScheduleV1 (UpdateRateCardNamedSchedulePayload updateRateCardNamedSchedulePayload = null)

Update a rate card's named schedule

Update a named schedule for the given rate card. This endpoint's availability is dependent on your client's configuration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateRateCardNamedSchedulePayload** | [**UpdateRateCardNamedSchedulePayload**](UpdateRateCardNamedSchedulePayload.md) | The rate card, schedule name, date range, and value to set. | [optional]  |

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


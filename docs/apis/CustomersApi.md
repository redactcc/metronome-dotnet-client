# Org.OpenAPITools.Api.CustomersApi

All URIs are relative to *https://api.metronome.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveCustomerBillingProviderConfigurationsV1**](CustomersApi.md#archivecustomerbillingproviderconfigurationsv1) | **POST** /v1/archiveCustomerBillingProviderConfigurations | Archive billing provider configurations for a customer |
| [**ArchiveCustomerRevenueSystemConfigurationsV1**](CustomersApi.md#archivecustomerrevenuesystemconfigurationsv1) | **POST** /v1/archiveCustomerRevenueSystemConfigurations | Archive revenue system configurations for a customer |
| [**ArchiveCustomerV1**](CustomersApi.md#archivecustomerv1) | **POST** /v1/customers/archive | Archive a customer |
| [**CreateCustomerV1**](CustomersApi.md#createcustomerv1) | **POST** /v1/customers | Create a customer |
| [**EmbeddableDashboardV1**](CustomersApi.md#embeddabledashboardv1) | **POST** /v1/dashboards/getEmbeddableUrl | Get an embeddable customer dashboard |
| [**GetCustomerBillingProviderConfigurationsV1**](CustomersApi.md#getcustomerbillingproviderconfigurationsv1) | **POST** /v1/getCustomerBillingProviderConfigurations | Fetch billing provider configurations for a customer |
| [**GetCustomerRevenueSystemConfigurationsV1**](CustomersApi.md#getcustomerrevenuesystemconfigurationsv1) | **POST** /v1/getCustomerRevenueSystemConfigurations | Fetch revenue system configurations for a customer |
| [**GetCustomerV1**](CustomersApi.md#getcustomerv1) | **GET** /v1/customers/{customer_id} | Get a customer |
| [**ListCustomersV1**](CustomersApi.md#listcustomersv1) | **GET** /v1/customers | List customers |
| [**SetCustomerBillableStatusV1**](CustomersApi.md#setcustomerbillablestatusv1) | **POST** /v1/customers/setBillableStatus | Set customer billable status |
| [**SetCustomerBillingProviderConfigurationsV1**](CustomersApi.md#setcustomerbillingproviderconfigurationsv1) | **POST** /v1/setCustomerBillingProviderConfigurations | Set billing provider configurations for a customer |
| [**SetCustomerNameV1**](CustomersApi.md#setcustomernamev1) | **POST** /v1/customers/{customer_id}/setName | Update a customer name |
| [**SetCustomerRevenueSystemConfigurationsV1**](CustomersApi.md#setcustomerrevenuesystemconfigurationsv1) | **POST** /v1/setCustomerRevenueSystemConfigurations | Set revenue system configurations for a customer |
| [**SetIngestAliasesV1**](CustomersApi.md#setingestaliasesv1) | **POST** /v1/customers/{customer_id}/setIngestAliases | Create or update customer ingest aliases |
| [**UpdateCustomerConfigV1**](CustomersApi.md#updatecustomerconfigv1) | **POST** /v1/customers/{customer_id}/updateConfig | Update a customer configuration |

<a id="archivecustomerbillingproviderconfigurationsv1"></a>
# **ArchiveCustomerBillingProviderConfigurationsV1**
> ArchiveCustomerBillingProviderConfigurationsV1200Response ArchiveCustomerBillingProviderConfigurationsV1 (CustomerBillingProviderArchivePayload customerBillingProviderArchivePayload = null)

Archive billing provider configurations for a customer

Deprecate an existing billing configuration for a customer to handle churn or billing and collection preference changes. Archiving a billing configuration takes effect immediately. If there are active contracts using the configuration, Metronome will archive the configuration on the contract and immediately stop metering to downstream systems.  ### Use this endpoint to: - Remove billing provider customer data and configurations when no longer needed - Clean up test or deprecated billing provider configurations - Free up uniqueness keys for reuse with new billing provider configurations - Disable threshold recharge configurations associated with archived billing providers  ### Key response fields: A successful response returns: - `success`: Boolean indicating the operation completed successfully - `error`: Null on success, error message on failure  ### Usage guidelines: - Archiving a contract configuration during a grace period will result in the invoice not being sent to the customer - Automatically disables both spend-based and credit-based threshold recharge configurations for contracts using the archived billing provider         - You can archive multiple configurations for a single customer in a single request, but any validation failures for an individual configuration will prevent the entire operation from succeeding 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerBillingProviderArchivePayload** | [**CustomerBillingProviderArchivePayload**](CustomerBillingProviderArchivePayload.md) | The ids of the billing provider configurations to archive | [optional]  |

### Return type

[**ArchiveCustomerBillingProviderConfigurationsV1200Response**](ArchiveCustomerBillingProviderConfigurationsV1200Response.md)

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
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="archivecustomerrevenuesystemconfigurationsv1"></a>
# **ArchiveCustomerRevenueSystemConfigurationsV1**
> ArchiveCustomerRevenueSystemConfigurationsV1200Response ArchiveCustomerRevenueSystemConfigurationsV1 (CustomerRevenueSystemArchivePayload customerRevenueSystemArchivePayload = null)

Archive revenue system configurations for a customer

Archive existing revenue system configurations for a customer. Archiving a revenue system configuration takes effect immediately.  ### Use this endpoint to: - Remove revenue system configurations when no longer needed - Clean up test or deprecated revenue system configurations  ### Key response fields: A successful response returns: - `customer_id`: The customer ID the configurations belong to - `customer_revenue_system_configuration_ids`: The archived configuration IDs 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerRevenueSystemArchivePayload** | [**CustomerRevenueSystemArchivePayload**](CustomerRevenueSystemArchivePayload.md) | The ids of the revenue system configurations to archive | [optional]  |

### Return type

[**ArchiveCustomerRevenueSystemConfigurationsV1200Response**](ArchiveCustomerRevenueSystemConfigurationsV1200Response.md)

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
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="archivecustomerv1"></a>
# **ArchiveCustomerV1**
> ArchiveAlertV1200Response ArchiveCustomerV1 (Id id = null)

Archive a customer

Use this endpoint to archive a customer while preserving auditability. Archiving a customer will automatically archive all contracts as of the current date and void all corresponding invoices. Use this endpoint if a customer is onboarded by mistake.  ### Usage guidelines: - Once a customer is archived, it cannot be unarchived. - Archived customers can still be viewed through the API or the UI for audit purposes.  - Ingest aliases remain idempotent for archived customers. In order to reuse an ingest alias, first remove the ingest alias from the customer prior to archiving. - Any notifications associated with the customer will no longer be triggered. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | [**Id**](Id.md) | The ID of the customer to archive | [optional]  |

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

<a id="createcustomerv1"></a>
# **CreateCustomerV1**
> CreateCustomerV1200Response CreateCustomerV1 (LegacyCreateCustomerPayload legacyCreateCustomerPayload = null)

Create a customer

Create a new customer in Metronome and optionally the billing configuration (recommended) which dictates where invoices for the customer will be sent or where payment will be collected.   ### Use this endpoint to: Execute your customer provisioning workflows for either PLG motions, where customers originate in your platform, or SLG motions, where customers originate in your sales system.  ### Key response fields:  This end-point returns the `customer_id` created by the request. This id can be used to fetch relevant billing configurations and create contracts.  ### Example workflow: - Generally, Metronome recommends first creating the customer in the downstream payment / ERP system when payment method is collected and then creating the customer in Metronome using the response (i.e. `customer_id`) from the downstream system. If you do not create a billing configuration on customer creation, you can add it later.         - Once a customer is created, you can then create a contract for the customer. In the contract creation process, you will need to add the customer billing configuration to the contract to ensure Metronome invoices the customer correctly. This is because a customer can have multiple configurations. - As part of the customer creation process, set the ingest alias for the customer which will ensure usage is accurately mapped to the customer. Ingest aliases can be added or changed after the creation process as well.  ### Usage guidelines: For details on different billing configurations for different systems, review the `/setCustomerBillingConfiguration` end-point. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **legacyCreateCustomerPayload** | [**LegacyCreateCustomerPayload**](LegacyCreateCustomerPayload.md) | The customer to create | [optional]  |

### Return type

[**CreateCustomerV1200Response**](CreateCustomerV1200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **409** | A customer with this ID already exists |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="embeddabledashboardv1"></a>
# **EmbeddableDashboardV1**
> EmbeddableDashboardV1200Response EmbeddableDashboardV1 (EmbeddableDashboardPayload embeddableDashboardPayload = null)

Get an embeddable customer dashboard

Generate secure, embeddable dashboard URLs that allow you to seamlessly integrate Metronome's billing visualizations directly into your application. This endpoint creates authenticated iframe-ready URLs for customer-specific dashboards, providing a white-labeled billing experience without building custom UI.  ### Use this endpoint to: - Embed billing dashboards directly in your customer portal or admin interface - Provide self-service access to invoices, usage data, and credit balances - Build white-labeled billing experiences with minimal development effort  ### Key response fields: - A secure, time-limited URL that can be embedded in an iframe - The URL includes authentication tokens and configuration parameters - URLs are customer-specific and respect your security settings  ### Usage guidelines: - Dashboard types: Choose from `invoices`, `usage`, or `commits_and_credits` - Customization options:     - `dashboard_options`: Configure dashboard behavior. Supported for the invoices dashboard only. Available keys include: `show_zero_usage_line_items` (\"true\"/\"false\"), `contract_id` (UUID, filters invoices by contract), `invoice_type` (\"USAGE\" or \"SCHEDULED\", filters by invoice type), and `invoice_status_filter` (\"VOID\", \"FINALIZED\", \"DRAFT\", \"FINALIZED_AND_DRAFT\", or \"ALL\")     - `color_overrides`: Match your brand's color palette - Iframe implementation: Embed the returned URL directly in an iframe element - Responsive design: Dashboards automatically adapt to container dimensions 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **embeddableDashboardPayload** | [**EmbeddableDashboardPayload**](EmbeddableDashboardPayload.md) | The details of the dashboard to retrieve | [optional]  |

### Return type

[**EmbeddableDashboardV1200Response**](EmbeddableDashboardV1200Response.md)

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

<a id="getcustomerbillingproviderconfigurationsv1"></a>
# **GetCustomerBillingProviderConfigurationsV1**
> GetCustomerBillingProviderConfigurationsV1200Response GetCustomerBillingProviderConfigurationsV1 (GetCustomerBillingProviderConfigurationsV1Request getCustomerBillingProviderConfigurationsV1Request = null)

Fetch billing provider configurations for a customer

Returns all billing configurations previously set for the customer. Use during the contract provisioning process to fetch the `billing_provider_configuration_id` needed to set the contract billing configuration. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **getCustomerBillingProviderConfigurationsV1Request** | [**GetCustomerBillingProviderConfigurationsV1Request**](GetCustomerBillingProviderConfigurationsV1Request.md) | The customer id for which to fetch billing provider configurations | [optional]  |

### Return type

[**GetCustomerBillingProviderConfigurationsV1200Response**](GetCustomerBillingProviderConfigurationsV1200Response.md)

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

<a id="getcustomerrevenuesystemconfigurationsv1"></a>
# **GetCustomerRevenueSystemConfigurationsV1**
> GetCustomerRevenueSystemConfigurationsV1200Response GetCustomerRevenueSystemConfigurationsV1 (GetCustomerRevenueSystemConfigurationsV1Request getCustomerRevenueSystemConfigurationsV1Request = null)

Fetch revenue system configurations for a customer

Returns all revenue system configurations previously set for the customer. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **getCustomerRevenueSystemConfigurationsV1Request** | [**GetCustomerRevenueSystemConfigurationsV1Request**](GetCustomerRevenueSystemConfigurationsV1Request.md) | The customer id for which to fetch revenue system configurations | [optional]  |

### Return type

[**GetCustomerRevenueSystemConfigurationsV1200Response**](GetCustomerRevenueSystemConfigurationsV1200Response.md)

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

<a id="getcustomerv1"></a>
# **GetCustomerV1**
> GetCustomerV1200Response GetCustomerV1 (Guid customerId)

Get a customer

Get detailed information for a specific customer by their Metronome ID. Returns customer profile data including name, creation date, ingest aliases, configuration settings, and custom fields. Use this endpoint to fetch complete customer details for billing operations or account management.  Note: If searching for a customer billing configuration, use the `/getCustomerBillingConfigurations` endpoint. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **Guid** |  |  |

### Return type

[**GetCustomerV1200Response**](GetCustomerV1200Response.md)

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

<a id="listcustomersv1"></a>
# **ListCustomersV1**
> ListCustomersV1200Response ListCustomersV1 (int limit = null, string nextPage = null, string ingestAlias = null, List<string> customerIds = null, bool onlyArchived = null, List<string> salesforceAccountIds = null)

List customers

Gets a paginated list of all customers in your Metronome account. Use this endpoint to browse your customer base, implement customer search functionality, or sync customer data with external systems. Returns customer details including IDs, names, and configuration settings. Supports filtering and pagination parameters for efficient data retrieval. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int** | Max number of results that should be returned | [optional]  |
| **nextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional]  |
| **ingestAlias** | **string** | Filter the customer list by ingest_alias | [optional]  |
| **customerIds** | [**List&lt;string&gt;**](string.md) | Filter the customer list by customer_id.  Up to 100 ids can be provided. | [optional]  |
| **onlyArchived** | **bool** | Filter the customer list to only return archived customers. By default, only active customers are returned. | [optional]  |
| **salesforceAccountIds** | [**List&lt;string&gt;**](string.md) | Filter the customer list by salesforce_account_id.  Up to 100 ids can be provided. | [optional]  |

### Return type

[**ListCustomersV1200Response**](ListCustomersV1200Response.md)

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

<a id="setcustomerbillablestatusv1"></a>
# **SetCustomerBillableStatusV1**
> SetCustomerBillableStatusV1200Response SetCustomerBillableStatusV1 (SetCustomerBillableStatusPayload setCustomerBillableStatusPayload = null)

Set customer billable status

Set a customer's billable status. This endpoint's availability is dependent on your client's configuration. Metronome 1.0 plan invoices are not supported.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **setCustomerBillableStatusPayload** | [**SetCustomerBillableStatusPayload**](SetCustomerBillableStatusPayload.md) |  | [optional]  |

### Return type

[**SetCustomerBillableStatusV1200Response**](SetCustomerBillableStatusV1200Response.md)

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

<a id="setcustomerbillingproviderconfigurationsv1"></a>
# **SetCustomerBillingProviderConfigurationsV1**
> SetCustomerBillingProviderConfigurationsV1200Response SetCustomerBillingProviderConfigurationsV1 (SetCustomerBillingProviderConfigurationsV1Request setCustomerBillingProviderConfigurationsV1Request = null)

Set billing provider configurations for a customer

Create a billing configuration for a customer. Once created, these configurations are available to associate to a contract and dictates which downstream system to collect payment in or send the invoice to. You can create multiple configurations per customer. The configuration formats are distinct for each downstream provider.  ### Use this endpoint to: - Add the initial configuration to an existing customer. Once created, the billing configuration can then be associated to the customer's contract. - Add a new configuration to an existing customer. This might be used as part of an upgrade or downgrade workflow where the customer was previously billed through system A (e.g. Stripe) but will now be billed through system B (e.g. AWS). Once created, the new configuration can then be associated to the customer's contract. - Multiple configurations can be added per destination. For example, you can create two Stripe billing configurations for a Metronome customer that each have a distinct `collection_method`.  ### Delivery method options: - `direct_to_billing_provider`: Use when Metronome should send invoices directly to the billing provider's API (e.g., Stripe, NetSuite). This is the most common method for automated billing workflows. - `tackle`: Use specifically for AWS Marketplace transactions that require Tackle's co-selling platform for partner attribution and commission tracking. - `aws_sqs`: Use when you want invoice data delivered to an AWS SQS queue for custom processing before sending to your billing system. - `aws_sns`: Use when you want invoice notifications published to an AWS SNS topic for event-driven billing workflows.  ### Key response fields:  The id for the customer billing configuration. This id can be used to associate the billing configuration to a contract.  ### Usage guidelines: Must use the `delivery_method_id` if you have multiple Stripe accounts connected to Metronome. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **setCustomerBillingProviderConfigurationsV1Request** | [**SetCustomerBillingProviderConfigurationsV1Request**](SetCustomerBillingProviderConfigurationsV1Request.md) | The details of the billing provider configurations to insert | [optional]  |

### Return type

[**SetCustomerBillingProviderConfigurationsV1200Response**](SetCustomerBillingProviderConfigurationsV1200Response.md)

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
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="setcustomernamev1"></a>
# **SetCustomerNameV1**
> CreateCustomerV1200Response SetCustomerNameV1 (Guid customerId, SetCustomerNamePayload setCustomerNamePayload = null)

Update a customer name

Updates the display name for a customer record. Use this to correct customer names, update business names after rebranding, or maintain accurate customer information for invoicing and reporting. Returns the updated customer object with the new name applied immediately across all billing documents and interfaces. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **Guid** |  |  |
| **setCustomerNamePayload** | [**SetCustomerNamePayload**](SetCustomerNamePayload.md) | The customer name | [optional]  |

### Return type

[**CreateCustomerV1200Response**](CreateCustomerV1200Response.md)

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

<a id="setcustomerrevenuesystemconfigurationsv1"></a>
# **SetCustomerRevenueSystemConfigurationsV1**
> GetCustomerRevenueSystemConfigurationsV1200Response SetCustomerRevenueSystemConfigurationsV1 (SetCustomerRevenueSystemConfigurationsV1Request setCustomerRevenueSystemConfigurationsV1Request = null)

Set revenue system configurations for a customer

Create a revenue system configuration for a customer. Once created, these configurations are available to associate to a contract and dictates which downstream system to use for revenue workflows. The configuration formats are distinct for each downstream provider.  ### Use this endpoint to: - Add the initial configuration to an existing customer. Once created, the revenue system configuration can then be associated to the customer's contract. - Add a new configuration to an existing customer.  ### Key response fields:  Returns the inserted configuration objects, including the id of the revenue system configuration(s). These ids can be used to associate a revenue system to a contract. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **setCustomerRevenueSystemConfigurationsV1Request** | [**SetCustomerRevenueSystemConfigurationsV1Request**](SetCustomerRevenueSystemConfigurationsV1Request.md) | The details of the revenue system configurations to insert | [optional]  |

### Return type

[**GetCustomerRevenueSystemConfigurationsV1200Response**](GetCustomerRevenueSystemConfigurationsV1200Response.md)

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
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="setingestaliasesv1"></a>
# **SetIngestAliasesV1**
> void SetIngestAliasesV1 (Guid customerId, SetIngestAliasesPayload setIngestAliasesPayload = null)

Create or update customer ingest aliases

Sets the ingest aliases for a customer. Use this endpoint to associate a Metronome customer with an internal ID for easier tracking between systems. Ingest aliases can be used in the `customer_id` field when sending usage events to Metronome.   ### Usage guidelines: - This call is idempotent and fully replaces the set of ingest aliases for the given customer. - Switching an ingest alias from one customer to another will associate all corresponding usage to the new customer. - Use multiple ingest aliases to model child organizations within a single Metronome customer. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **Guid** |  |  |
| **setIngestAliasesPayload** | [**SetIngestAliasesPayload**](SetIngestAliasesPayload.md) | The aliases to add | [optional]  |

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

<a id="updatecustomerconfigv1"></a>
# **UpdateCustomerConfigV1**
> void UpdateCustomerConfigV1 (Guid customerId, CustomerConfigPayload customerConfigPayload = null)

Update a customer configuration

Update configuration settings for a specific customer, such as external system integrations (e.g., Salesforce account ID) and other customer-specific billing parameters. Use this endpoint to modify customer configurations without affecting core customer data like name or ingest aliases. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **Guid** |  |  |
| **customerConfigPayload** | [**CustomerConfigPayload**](CustomerConfigPayload.md) | The configuration for a specific customer | [optional]  |

### Return type

void (empty response body)

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


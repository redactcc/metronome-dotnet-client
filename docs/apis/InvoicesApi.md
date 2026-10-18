# Org.OpenAPITools.Api.InvoicesApi

All URIs are relative to *https://api.metronome.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ChargeSeatsV1**](InvoicesApi.md#chargeseatsv1) | **POST** /v1/customers/{customer_id}/invoices/invoice_seats | Invoice seats |
| [**GetInvoicePdfV1**](InvoicesApi.md#getinvoicepdfv1) | **GET** /v1/customers/{customer_id}/invoices/{invoice_id}/pdf | Get an invoice PDF |
| [**GetInvoiceV1**](InvoicesApi.md#getinvoicev1) | **GET** /v1/customers/{customer_id}/invoices/{invoice_id} | Get an invoice |
| [**ListBreakdownInvoicesV1**](InvoicesApi.md#listbreakdowninvoicesv1) | **GET** /v1/customers/{customer_id}/invoices/breakdowns | List invoice breakdowns |
| [**ListInvoicesV1**](InvoicesApi.md#listinvoicesv1) | **GET** /v1/customers/{customer_id}/invoices | List invoices |
| [**ListSpendBreakdownInvoicesV1**](InvoicesApi.md#listspendbreakdowninvoicesv1) | **POST** /v1/customers/{customer_id}/invoices/spend-breakdowns | List spend invoice breakdowns |
| [**PreviewCustomerEventsV1**](InvoicesApi.md#previewcustomereventsv1) | **POST** /v1/customers/{customer_id}/previewEvents | Preview events |
| [**RegenerateInvoiceV1**](InvoicesApi.md#regenerateinvoicev1) | **POST** /v1/invoices/regenerate | Regenerate an invoice |
| [**VoidInvoiceV1**](InvoicesApi.md#voidinvoicev1) | **POST** /v1/invoices/void | Void an invoice |

<a id="chargeseatsv1"></a>
# **ChargeSeatsV1**
> Invoice ChargeSeatsV1 (Guid customerId, ChargeSeatsV1Request chargeSeatsV1Request = null)

Invoice seats

Creates an prorated invoice for a seat addition. As an alternative to this endpoint, you can elect to use automatic seat invoicing feature. Metronome will check for new seat usage every hour and automatically invoice for any new seats. For newly created active customer plans, there will be up to 4 hour delay before the first automatic seat invoice is generated. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **Guid** |  |  |
| **chargeSeatsV1Request** | [**ChargeSeatsV1Request**](ChargeSeatsV1Request.md) | Invoice seats parameters. List of seat charges and additional seats to charge for. | [optional]  |

### Return type

[**Invoice**](Invoice.md)

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

<a id="getinvoicepdfv1"></a>
# **GetInvoicePdfV1**
> Object GetInvoicePdfV1 (Guid customerId, Guid invoiceId)

Get an invoice PDF

Retrieve a PDF version of a specific invoice by its unique identifier. This endpoint generates a professionally formatted invoice document suitable for sharing with customers, accounting teams, or for record-keeping purposes.  ### Use this endpoint to: - Provide customers with downloadable or emailable copies of their invoices - Support accounting and finance teams with official billing documents - Maintain accurate records of billing transactions for audits and compliance  ### Key response details: - The response is a binary PDF file representing the full invoice - The PDF includes all standard invoice information such as line items, totals, billing period, and customer details - The document is formatted for clarity and professionalism, suitable for official use  ### Usage guidelines: - Ensure the `invoice_id` corresponds to an existing invoice for the specified `customer_id` - The PDF is generated on-demand; frequent requests for the same invoice may impact performance - Use appropriate headers to handle the binary response in your application (e.g., setting `Content-Type: application/pdf`) 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **Guid** |  |  |
| **invoiceId** | **Guid** |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | The specified resource was not found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getinvoicev1"></a>
# **GetInvoiceV1**
> GetInvoiceV1200Response GetInvoiceV1 (Guid customerId, Guid invoiceId, bool skipZeroQtyLineItems = null)

Get an invoice

Retrieve detailed information for a specific invoice by its unique identifier. This endpoint returns comprehensive invoice data including line items, applied credits, totals, and billing period details for both finalized and draft invoices.  ### Use this endpoint to: - Display historical invoice details in customer-facing dashboards or billing portals. - Retrieve current month draft invoices to show customers their month-to-date spend. - Access finalized invoices for historical billing records and payment reconciliation. - Validate customer pricing and credit applications for customer support queries.   ### Key response fields:  Invoice status (DRAFT, FINALIZED, VOID) Billing period start and end dates Total amount and amount due after credits Detailed line items broken down by: - Customer and contract information - Invoice line item type - Product/service name and ID - Quantity consumed - Unit and total price  - Time period for usage-based charges - Applied credits or prepaid commitments   ### Usage guidelines: - Draft invoices update in real-time as usage is reported and may change before finalization - The response includes both usage-based line items (e.g., API calls, data processed) and scheduled charges (e.g., monthly subscriptions, commitment fees) - Credit and commitment applications are shown as separate line items with negative amounts - For voided invoices, the response will indicate VOID status but retain all original line item details 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **Guid** |  |  |
| **invoiceId** | **Guid** |  |  |
| **skipZeroQtyLineItems** | **bool** | If set, all zero quantity line items will be filtered out of the response | [optional]  |

### Return type

[**GetInvoiceV1200Response**](GetInvoiceV1200Response.md)

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

<a id="listbreakdowninvoicesv1"></a>
# **ListBreakdownInvoicesV1**
> ListBreakdownInvoicesV1200Response ListBreakdownInvoicesV1 (Guid customerId, DateTime startingOn, DateTime endingBefore, string nextPage = null, string status = null, bool skipZeroQtyLineItems = null, int limit = null, string windowSize = null, string sort = null, string creditTypeId = null)

List invoice breakdowns

Retrieve granular time-series breakdowns of invoice data at hourly or daily intervals. This endpoint transforms standard invoices into detailed timelines, enabling you to track usage patterns, identify consumption spikes, and provide customers with transparency into their billing details throughout the billing period.  ### Use this endpoint to: - Build usage analytics dashboards showing daily or hourly consumption trends - Identify peak usage periods for capacity planning and cost optimization - Generate detailed billing reports for finance teams and customer success - Troubleshoot billing disputes by examining usage patterns at specific times - Power real-time cost monitoring and alerting systems  ### Key response fields: An array of BreakdownInvoice objects, each containing: - All standard invoice fields (ID, customer, commit, line items, totals, status) - Line items with quantities and costs for that specific period - `breakdown_start_timestamp`: Start of the specific time window - `breakdown_end_timestamp`: End of the specific time window - `next_page`: Pagination cursor for large result sets  ### Usage guidelines: - Time granularity: Set `window_size` to hour or day based on your analysis needs - Response limits: Daily breakdowns return up to 35 days; hourly breakdowns return up to 24 hours per request - Date filtering: Use `starting_on` and `ending_before` to focus on specific periods - Performance: For large date ranges, use pagination to retrieve all data efficiently - Backdated usage: If usage events arrive after invoice finalization, breakdowns will reflect the updated usage - Zero quantity filtering: Use `skip_zero_qty_line_items=true` to exclude periods with no usage


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **Guid** |  |  |
| **startingOn** | **DateTime** | RFC 3339 timestamp. Breakdowns will only be returned for time windows that start on or after this time. |  |
| **endingBefore** | **DateTime** | RFC 3339 timestamp. Breakdowns will only be returned for time windows that end on or before this time. |  |
| **nextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional]  |
| **status** | **string** | Invoice status, e.g. DRAFT or FINALIZED | [optional]  |
| **skipZeroQtyLineItems** | **bool** | If set, all zero quantity line items will be filtered out of the response | [optional]  |
| **limit** | **int** | Max number of results that should be returned. For daily breakdowns, the response can return up to 35 days worth of breakdowns. For hourly breakdowns, the response can return up to 24 hours. If there are more results, a cursor to the next page is returned. | [optional]  |
| **windowSize** | **string** | The granularity of the breakdowns to return. Defaults to day. | [optional]  |
| **sort** | **string** | Invoice sort order by issued_at, e.g. date_asc or date_desc.  Defaults to date_asc. | [optional]  |
| **creditTypeId** | **string** | Only return invoices for the specified credit type | [optional]  |

### Return type

[**ListBreakdownInvoicesV1200Response**](ListBreakdownInvoicesV1200Response.md)

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

<a id="listinvoicesv1"></a>
# **ListInvoicesV1**
> ListInvoicesV1200Response ListInvoicesV1 (Guid customerId, int limit = null, string nextPage = null, string status = null, string type = null, bool skipZeroQtyLineItems = null, string sort = null, string creditTypeId = null, Guid contractId = null, DateTime startingOn = null, DateTime endingBefore = null, string webhookNotificationId = null, bool includeHistoricalCommitInvoices = null)

List invoices

Retrieves a paginated list of invoices for a specific customer, with flexible filtering options to narrow results by status, date range, credit type, and more. This endpoint provides a comprehensive view of a customer's billing history and current charges, supporting both real-time billing dashboards and historical reporting needs.  ### Use this endpoint to: - Display historical invoice details in customer-facing dashboards or billing portals. - Retrieve current month draft invoices to show customers their month-to-date spend. - Access finalized invoices for historical billing records and payment reconciliation. - Validate customer pricing and credit applications for customer support queries.  - Generate financial reports by filtering invoices within specific date ranges  ### Key response fields: Array of invoice objects containing: - Invoice ID and status (DRAFT, FINALIZED, VOID) - Invoice type (USAGE, SCHEDULED) - Billing period start and end dates - Issue date and due date - Total amount, subtotal, and amount due - Applied credits summary - Contract ID reference - External billing provider status (if integrated with Stripe, etc.) - Pagination metadata `next_page` cursor  ### Usage guidelines: - The endpoint returns invoice summaries; use the Get Invoice endpoint for detailed line items - Draft invoices are continuously updated as new usage is reported and will show real-time spend - Results are ordered by creation date descending by default (newest first) - When filtering by date range, the filter applies to the billing period, not the issue date - For customers with many invoices, implement pagination to ensure all results are retrieved External billing provider statuses (like Stripe payment status) are included when applicable - Voided invoices are included in results by default unless filtered out by status 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **Guid** |  |  |
| **limit** | **int** | Max number of results that should be returned | [optional]  |
| **nextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional]  |
| **status** | **string** | Invoice status, e.g. DRAFT, FINALIZED, or VOID | [optional]  |
| **type** | **string** | Filter invoices by type. Defaults to returning all invoice types. | [optional]  |
| **skipZeroQtyLineItems** | **bool** | If set, all zero quantity line items will be filtered out of the response | [optional]  |
| **sort** | **string** | Invoice sort order by issued_at, e.g. date_asc or date_desc.  Defaults to date_asc. | [optional]  |
| **creditTypeId** | **string** | Only return invoices for the specified credit type | [optional]  |
| **contractId** | **Guid** | Only return invoices for the specified contract | [optional]  |
| **startingOn** | **DateTime** | RFC 3339 timestamp (inclusive). Invoices will only be returned for billing periods that start at or after this time. | [optional]  |
| **endingBefore** | **DateTime** | RFC 3339 timestamp (exclusive). Invoices will only be returned for billing periods that end before this time. | [optional]  |
| **webhookNotificationId** | **string** | Indicates that this API request was triggered by a webhook notification with the provided ID. | [optional]  |
| **includeHistoricalCommitInvoices** | **bool** | When true, includes historical commit invoices alongside active invoices. Defaults to false. | [optional] [default to false] |

### Return type

[**ListInvoicesV1200Response**](ListInvoicesV1200Response.md)

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

<a id="listspendbreakdowninvoicesv1"></a>
# **ListSpendBreakdownInvoicesV1**
> ListSpendBreakdownInvoicesV1200Response ListSpendBreakdownInvoicesV1 (Guid customerId, bool includeListPrices = null, SpendBreakdownInvoicesQueryPayload spendBreakdownInvoicesQueryPayload = null)

List spend invoice breakdowns

Granularly analyze customer spend patterns by dynamically slicing and dicing costs across any dimension. This endpoint empowers you to break down spending by granular properties like user, organization, model, region, or any custom event property—even if these aren't the default groupings on your invoices. Unlike standard invoice breakdowns, this endpoint focuses purely on spend analysis, making helpful for building powerful cost analytics dashboards that show spend before credit/commit application.  ### Use this endpoint to: - Identify cost drivers: Pinpoint which users, teams, or resources are driving the most spend - Build usage analytics dashboards: Let customers explore their costs by any event property (user_id, org_id, model_id, region, etc.) - Enable showback/chargeback: Allocate costs to specific departments, projects, or cost centers - Detect anomalies: Find unexpected spending patterns by analyzing costs across different dimensions - Optimize resource usage: Help customers identify underutilized or over-provisioned resources - Support multi-tenancy: Show spending breakdowns for specific organizations within a single account - Create custom reports: Generate executive dashboards with spending by any business-relevant dimension  ### Key response fields: Spend-focused invoice data with: - Pure spend information: No commits or credits—just raw spending data for cleaner analysis - Dynamic grouping: Line items grouped by your specified group_keys (overriding default presentation groups) - Filtered results: Only line items matching your group_filters criteria - Flexible time windows: Daily, hourly, or full-period (none) breakdowns - Complete line item details: Including quantities, unit prices, and custom presentation group values  ### Usage guidelines: - Group key setup: All keys used in group_keys, group_filters, and pricing groups must exist in the same compound group key on the billable metric - Supported window sizes: hour, day, or none (for full period analysis) - Filtering power: Use group_filters to focus on specific values (e.g., only show data for specific user_ids) - Override flexibility: Change how costs are grouped without affecting actual invoicing  Limitations: - Cannot override group keys when using:   - MAX aggregation billable metrics   - Tiered pricing   - Quantity rounding   - Commit-specific overrides   - Overrides on presentation group values


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **Guid** |  |  |
| **includeListPrices** | **bool** | If set, list prices will be returned for each contract usage and subscription line item. | [optional]  |
| **spendBreakdownInvoicesQueryPayload** | [**SpendBreakdownInvoicesQueryPayload**](SpendBreakdownInvoicesQueryPayload.md) |  | [optional]  |

### Return type

[**ListSpendBreakdownInvoicesV1200Response**](ListSpendBreakdownInvoicesV1200Response.md)

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

<a id="previewcustomereventsv1"></a>
# **PreviewCustomerEventsV1**
> PreviewCustomerEventsV1200Response PreviewCustomerEventsV1 (Guid customerId, PreviewEventsPayload previewEventsPayload = null)

Preview events

Preview how a set of events will affect a customer's invoices. Generates draft invoices for a customer using their current contract configuration and the provided events.  This is useful for testing how new events will affect the customer's invoices before they are actually processed. Customers on contracts with SQL billable metrics are not supported. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **Guid** |  |  |
| **previewEventsPayload** | [**PreviewEventsPayload**](PreviewEventsPayload.md) | The events to preview | [optional]  |

### Return type

[**PreviewCustomerEventsV1200Response**](PreviewCustomerEventsV1200Response.md)

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

<a id="regenerateinvoicev1"></a>
# **RegenerateInvoiceV1**
> RegenerateInvoiceV1200Response RegenerateInvoiceV1 (RegenerateInvoiceV1Request regenerateInvoiceV1Request = null)

Regenerate an invoice

This endpoint regenerates a voided invoice and recalculates the invoice based on up-to-date rates, available balances, and other fees regardless of the billing period.  ### Use this endpoint to: Recalculate an invoice with updated rate terms, available balance, and fees to correct billing disputes or discrepancies  ### Key response fields: The regenerated invoice id, which is distinct from the previously voided invoice.  ### Usage guidelines: If an invoice is attached to a contract with a billing provider on it, the regenerated invoice will be distributed based on the configuration. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **regenerateInvoiceV1Request** | [**RegenerateInvoiceV1Request**](RegenerateInvoiceV1Request.md) | The invoice id to regenerate | [optional]  |

### Return type

[**RegenerateInvoiceV1200Response**](RegenerateInvoiceV1200Response.md)

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

<a id="voidinvoicev1"></a>
# **VoidInvoiceV1**
> VoidInvoiceV1200Response VoidInvoiceV1 (VoidInvoiceV1Request voidInvoiceV1Request = null)

Void an invoice

Permanently cancels an invoice by setting its status to voided, preventing collection and removing it from customer billing. Use this to correct billing errors, cancel incorrect charges, or handle disputed invoices that should not be collected. Returns the voided invoice ID with the status change applied immediately to stop any payment processing. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **voidInvoiceV1Request** | [**VoidInvoiceV1Request**](VoidInvoiceV1Request.md) | The invoice id to void | [optional]  |

### Return type

[**VoidInvoiceV1200Response**](VoidInvoiceV1200Response.md)

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


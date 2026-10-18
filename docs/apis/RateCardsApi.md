# Org.OpenAPITools.Api.RateCardsApi

All URIs are relative to *https://api.metronome.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddRateV1**](RateCardsApi.md#addratev1) | **POST** /v1/contract-pricing/rate-cards/addRate | Add a rate |
| [**AddRatesV1**](RateCardsApi.md#addratesv1) | **POST** /v1/contract-pricing/rate-cards/addRates | Add rates |
| [**ArchiveRateCardV1**](RateCardsApi.md#archiveratecardv1) | **POST** /v1/contract-pricing/rate-cards/archive | Archive a rate card |
| [**CreateRateCardV1**](RateCardsApi.md#createratecardv1) | **POST** /v1/contract-pricing/rate-cards/create | Create a rate card |
| [**GetRateCardV1**](RateCardsApi.md#getratecardv1) | **POST** /v1/contract-pricing/rate-cards/get | Get a rate card |
| [**GetRateScheduleV1**](RateCardsApi.md#getrateschedulev1) | **POST** /v1/contract-pricing/rate-cards/getRateSchedule | Get a rate schedule |
| [**GetRatesV1**](RateCardsApi.md#getratesv1) | **POST** /v1/contract-pricing/rate-cards/getRates | Get rates |
| [**ListRateCardsV1**](RateCardsApi.md#listratecardsv1) | **POST** /v1/contract-pricing/rate-cards/list | List rate cards |
| [**MoveRateCardProductsV1**](RateCardsApi.md#moveratecardproductsv1) | **POST** /v1/contract-pricing/rate-cards/moveRateCardProducts | Update the rate card products order |
| [**SetRateCardProductsOrderV1**](RateCardsApi.md#setratecardproductsorderv1) | **POST** /v1/contract-pricing/rate-cards/setRateCardProductsOrder | Set the rate card products order |
| [**UpdateRateCardV1**](RateCardsApi.md#updateratecardv1) | **POST** /v1/contract-pricing/rate-cards/update | Update a rate card |

<a id="addratev1"></a>
# **AddRateV1**
> AddRateV1200Response AddRateV1 (AddRatePayload addRatePayload = null)

Add a rate

Add a new rate  This endpoint is heavily rate limited. For adding multiple rates, using the [addRates](https://docs.metronome.com/api-reference/rate-cards/add-rates) endpoint is strongly encouraged. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **addRatePayload** | [**AddRatePayload**](AddRatePayload.md) | Add a new rate | [optional]  |

### Return type

[**AddRateV1200Response**](AddRateV1200Response.md)

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

<a id="addratesv1"></a>
# **AddRatesV1**
> ArchiveAlertV1200Response AddRatesV1 (AddRatesV1Request addRatesV1Request = null)

Add rates

Add new rates 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **addRatesV1Request** | [**AddRatesV1Request**](AddRatesV1Request.md) | Add new rates | [optional]  |

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

<a id="archiveratecardv1"></a>
# **ArchiveRateCardV1**
> ArchiveAlertV1200Response ArchiveRateCardV1 (Id id = null)

Archive a rate card

Permanently disable a rate card by archiving it, preventing use in new contracts while preserving existing contract pricing. Use this when retiring old pricing models, consolidating rate cards, or removing outdated pricing structures. Returns the archived rate card ID and stops the rate card from appearing in contract creation workflows. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | [**Id**](Id.md) | The ID of the rate card to archive | [optional]  |

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

<a id="createratecardv1"></a>
# **CreateRateCardV1**
> ArchiveAlertV1200Response CreateRateCardV1 (CreateRateCardPayload createRateCardPayload = null)

Create a rate card

In Metronome, the rate card is the central location for your pricing. Rate cards were built with new product launches and pricing changes in mind - you can update your products and pricing in one place, and that change will be automatically propagated across your customer cohorts. Most clients need only maintain one or a few rate cards within Metronome.  ### Use this endpoint to: - Create a rate card with a name and description - Define the rate card's single underlying fiat currency, and any number of conversion rates between that fiat currency and custom pricing units. You can then add products and associated rates in the fiat currency or custom pricing unit for which you have defined a conversion rate.  - Set aliases for the rate card. Aliases are human-readable names that you can use in the place of the id of the rate card when provisioning a customer's contract. By using an alias, you can easily create a contract and provision a customer by choosing the paygo rate card, without storing the rate card id in your internal systems. This is helpful when launching a new rate card for paygo customers, you can update the alias for paygo to be scheduled to be assigned to the new rate card without updating your code.  ### Key response fields: - The ID of the rate card you just created  ### Usage guidelines: - After creating a rate card, you can now use the addRate or addRates endpoints to add products and their prices to it - A rate card alias can only be used by one rate card at a time. If you create a contract with a rate card alias that is already in use by another rate card, the original rate card's alias schedule will be updated. The alias will reference the rate card to which it was most recently assigned. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createRateCardPayload** | [**CreateRateCardPayload**](CreateRateCardPayload.md) | In Metronome, the rate card is the central location for your pricing. Rate cards were built with new product launches and pricing changes in mind - you can update your products and pricing in one place, and that change will be automatically propagated across your customer cohorts. Most clients need only maintain one or a few rate cards within Metronome.  ### Use this endpoint to: - Create a rate card with a name and description - Define the rate card&#39;s single underlying fiat currency, and any number of conversion rates between that fiat currency and custom pricing units. You can then add products and associated rates in the fiat currency or custom pricing unit for which you have defined a conversion rate.  - Set aliases for the rate card. Aliases are human-readable names that you can use in the place of the id of the rate card when provisioning a customer&#39;s contract. By using an alias, you can easily create a contract and provision a customer by choosing the paygo rate card, without storing the rate card id in your internal systems. This is helpful when launching a new rate card for paygo customers, you can update the alias for paygo to be scheduled to be assigned to the new rate card without updating your code.  ### Key response fields: - The ID of the rate card you just created  ### Usage guidelines: - After creating a rate card, you can now use the addRate or addRates endpoints to add products and their prices to it - A rate card alias can only be used by one rate card at a time. If you create a contract with a rate card alias that is already in use by another rate card, the original rate card&#39;s alias schedule will be updated. The alias will reference the rate card to which it was most recently assigned.  | [optional]  |

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

<a id="getratecardv1"></a>
# **GetRateCardV1**
> GetRateCardV1200Response GetRateCardV1 (Id id = null)

Get a rate card

Return details for a specific rate card including name, description, and aliases. This endpoint does not return rates - use the dedicated getRates or getRateSchedule endpoints to understand the rates on a rate card. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | [**Id**](Id.md) | The ID of the rate card to get | [optional]  |

### Return type

[**GetRateCardV1200Response**](GetRateCardV1200Response.md)

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

<a id="getrateschedulev1"></a>
# **GetRateScheduleV1**
> GetRateScheduleV1200Response GetRateScheduleV1 (int limit = null, string nextPage = null, GetRateSchedulePayload getRateSchedulePayload = null)

Get a rate schedule

A rate card defines the prices that you charge for your products. Rate cards support scheduled changes over time, to allow you to easily roll out pricing changes and new product launches across your customer base. Use this endpoint to understand the rate schedule `starting_at` a given date, optionally filtering the list of rates returned based on product id or pricing group values. For example, you may want to display a schedule of upcoming price changes for a given product in your product experience - use this endpoint to fetch that information from its source of truth in Metronome.   If you want to understand the rates for a specific customer's contract, inclusive of contract-level overrides, use the `getContractRateSchedule` endpoint. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int** | Max number of results that should be returned | [optional]  |
| **nextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional]  |
| **getRateSchedulePayload** | [**GetRateSchedulePayload**](GetRateSchedulePayload.md) | Rate schedule filter options. | [optional]  |

### Return type

[**GetRateScheduleV1200Response**](GetRateScheduleV1200Response.md)

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

<a id="getratesv1"></a>
# **GetRatesV1**
> GetRateScheduleV1200Response GetRatesV1 (int limit = null, string nextPage = null, GetRatesPayload getRatesPayload = null)

Get rates

Understand the rate schedule at a given timestamp, optionally filtering the list of rates returned based on properties such as `product_id` and `pricing_group_values`. For example, you may want to display the current price for a given product in your product experience - use this endpoint to fetch that information from its source of truth in Metronome.   If you want to understand the rates for a specific customer's contract, inclusive of contract-level overrides, use the `getContractRateSchedule` endpoint. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int** | Max number of results that should be returned | [optional]  |
| **nextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional]  |
| **getRatesPayload** | [**GetRatesPayload**](GetRatesPayload.md) | Rate schedule filter options. | [optional]  |

### Return type

[**GetRateScheduleV1200Response**](GetRateScheduleV1200Response.md)

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

<a id="listratecardsv1"></a>
# **ListRateCardsV1**
> ListRateCardsV1200Response ListRateCardsV1 (int limit = null, string nextPage = null, Object body = null)

List rate cards

List all rate cards. Returns rate card IDs, names, descriptions, aliases, and other details. To view the rates associated with a given rate card, use the getRates or getRateSchedule endpoints. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int** | Max number of results that should be returned | [optional]  |
| **nextPage** | **string** | Cursor that indicates where the next page of results should start. | [optional]  |
| **body** | **Object** |  | [optional]  |

### Return type

[**ListRateCardsV1200Response**](ListRateCardsV1200Response.md)

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

<a id="moveratecardproductsv1"></a>
# **MoveRateCardProductsV1**
> ArchiveAlertV1200Response MoveRateCardProductsV1 (MoveRateCardProductsPayload moveRateCardProductsPayload = null)

Update the rate card products order

The ordering of products on a rate card determines the order in which the products will appear on customers' invoices. Use this endpoint to set the order of specific products on the rate card by moving them relative to their current location. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **moveRateCardProductsPayload** | [**MoveRateCardProductsPayload**](MoveRateCardProductsPayload.md) | New rate card product ordering | [optional]  |

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

<a id="setratecardproductsorderv1"></a>
# **SetRateCardProductsOrderV1**
> ArchiveAlertV1200Response SetRateCardProductsOrderV1 (SetRateCardProductsOrderPayload setRateCardProductsOrderPayload = null)

Set the rate card products order

The ordering of products on a rate card determines the order in which the products will appear on customers' invoices. Use this endpoint to set the order of products on the rate card. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **setRateCardProductsOrderPayload** | [**SetRateCardProductsOrderPayload**](SetRateCardProductsOrderPayload.md) | New rate card product ordering | [optional]  |

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

<a id="updateratecardv1"></a>
# **UpdateRateCardV1**
> ArchiveAlertV1200Response UpdateRateCardV1 (UpdateRateCardPayload updateRateCardPayload = null)

Update a rate card

Update a rate card's name, description, aliases, and credit type conversion rates. This endpoint does not affect underlying pricing rates or schedules.  ### Use this endpoint to: - Rename rate cards: Update display names or descriptions for organizational clarity - Manage aliases: Add, modify, or schedule alias transitions for seamless and code-free rate card migrations - Update documentation: Keep rate card descriptions current with business context - Configure custom pricing units: Add credit type conversions to enable rates with different pricing units  #### Active contract impact: - Alias changes: Already-created contracts continue using their originally assigned rate cards. - Other changes made using this endpoint will only impact the Metronome UI.  #### Grandfathering existing PLG customer pricing: - Rate card aliases support scheduled transitions, enabling seamless rate card migrations for new customers, allowing existing customers to be grandfathered into their existing prices without code. Note that there are multiple mechanisms to support grandfathering in Metronome.   #### How scheduled aliases work for PLG grandfathering: Initial setup: - Add alias to current rate card: Assign a stable alias (e.g., \"standard-pricing\") to your active rate card - Reference alias during contract creation: Configure your self-serve workflow to create contracts using `rate_card_alias` instead of direct `rate_card_id` - Automatic resolution: New contracts referencing the alias automatically resolve to the rate card associated with the alias at the point in time of provisioning  #### Grandfathering process: - Create new rate card: Build your new rate card with updated pricing structure - Schedule alias transition: Add the same alias to the new rate card with a `starting_at` timestamp - Automatic cutover: Starting at the scheduled time, new contracts created in your PLG workflow using that alias will automatically reference the new rate card 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **updateRateCardPayload** | [**UpdateRateCardPayload**](UpdateRateCardPayload.md) | Update a rate card. Must provide at least one of name, description, aliases, or addCreditTypeConversions. | [optional]  |

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


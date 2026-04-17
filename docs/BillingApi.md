# BillingApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**adminClearEnterpriseOverride**](BillingApi.md#adminclearenterpriseoverride) | **DELETE** /v1/billing/admin/tenants/{tenant_id}/overrides | Admin Clear Enterprise Override Handler |
| [**adminSetEnterpriseOverride**](BillingApi.md#adminsetenterpriseoverride) | **PUT** /v1/billing/admin/tenants/{tenant_id}/overrides | Admin Set Enterprise Override Handler |
| [**cancelTenantSubscription**](BillingApi.md#canceltenantsubscription) | **POST** /v1/billing/subscription/cancel | Cancel Tenant Subscription Handler |
| [**createBillingCheckoutSession**](BillingApi.md#createbillingcheckoutsession) | **POST** /v1/billing/checkout-session | Create Billing Checkout Session Handler |
| [**createBillingPortalSession**](BillingApi.md#createbillingportalsession) | **POST** /v1/billing/portal-session | Create Billing Portal Session Handler |
| [**getCurrentUserUsage**](BillingApi.md#getcurrentuserusage) | **GET** /v1/billing/usage/me | Get Current User Usage Handler |
| [**getTenantSubscription**](BillingApi.md#gettenantsubscription) | **GET** /v1/billing/subscription | Get Tenant Subscription Handler |
| [**getTenantUsage**](BillingApi.md#gettenantusage) | **GET** /v1/billing/usage | Get Tenant Usage Handler |
| [**listBillingPlans**](BillingApi.md#listbillingplans) | **GET** /v1/billing/plans | List Billing Plans Handler |
| [**resumeTenantSubscription**](BillingApi.md#resumetenantsubscription) | **POST** /v1/billing/subscription/resume | Resume Tenant Subscription Handler |



## adminClearEnterpriseOverride

> TenantSubscriptionResponse adminClearEnterpriseOverride(tenantId, xKSPlatformAdminKey)

Admin Clear Enterprise Override Handler

Clear all enterprise overrides for a tenant (contract ended).

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '@knowledge-stack/ksapi';
import type { AdminClearEnterpriseOverrideRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new BillingApi();

  const body = {
    // string
    tenantId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    xKSPlatformAdminKey: xKSPlatformAdminKey_example,
  } satisfies AdminClearEnterpriseOverrideRequest;

  try {
    const data = await api.adminClearEnterpriseOverride(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **tenantId** | `string` |  | [Defaults to `undefined`] |
| **xKSPlatformAdminKey** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**TenantSubscriptionResponse**](TenantSubscriptionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## adminSetEnterpriseOverride

> TenantSubscriptionResponse adminSetEnterpriseOverride(tenantId, setEnterpriseOverrideRequest, xKSPlatformAdminKey)

Admin Set Enterprise Override Handler

Set per-tenant enterprise contract overrides (custom pricing/limits).

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '@knowledge-stack/ksapi';
import type { AdminSetEnterpriseOverrideRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new BillingApi();

  const body = {
    // string
    tenantId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // SetEnterpriseOverrideRequest
    setEnterpriseOverrideRequest: ...,
    // string (optional)
    xKSPlatformAdminKey: xKSPlatformAdminKey_example,
  } satisfies AdminSetEnterpriseOverrideRequest;

  try {
    const data = await api.adminSetEnterpriseOverride(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **tenantId** | `string` |  | [Defaults to `undefined`] |
| **setEnterpriseOverrideRequest** | [SetEnterpriseOverrideRequest](SetEnterpriseOverrideRequest.md) |  | |
| **xKSPlatformAdminKey** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**TenantSubscriptionResponse**](TenantSubscriptionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## cancelTenantSubscription

> TenantSubscriptionResponse cancelTenantSubscription(authorization, ksUat)

Cancel Tenant Subscription Handler

Cancel subscription at end of current period.

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '@knowledge-stack/ksapi';
import type { CancelTenantSubscriptionRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new BillingApi();

  const body = {
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies CancelTenantSubscriptionRequest;

  try {
    const data = await api.cancelTenantSubscription(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**TenantSubscriptionResponse**](TenantSubscriptionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createBillingCheckoutSession

> CreateCheckoutSessionResponse createBillingCheckoutSession(createCheckoutSessionRequest, authorization, ksUat)

Create Billing Checkout Session Handler

Create a Stripe Checkout session for upgrading to a paid plan.

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '@knowledge-stack/ksapi';
import type { CreateBillingCheckoutSessionRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new BillingApi();

  const body = {
    // CreateCheckoutSessionRequest
    createCheckoutSessionRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies CreateBillingCheckoutSessionRequest;

  try {
    const data = await api.createBillingCheckoutSession(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **createCheckoutSessionRequest** | [CreateCheckoutSessionRequest](CreateCheckoutSessionRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**CreateCheckoutSessionResponse**](CreateCheckoutSessionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createBillingPortalSession

> CreatePortalSessionResponse createBillingPortalSession(createPortalSessionRequest, authorization, ksUat)

Create Billing Portal Session Handler

Create a Stripe billing portal session (manage payment method, cancel).

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '@knowledge-stack/ksapi';
import type { CreateBillingPortalSessionRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new BillingApi();

  const body = {
    // CreatePortalSessionRequest
    createPortalSessionRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies CreateBillingPortalSessionRequest;

  try {
    const data = await api.createBillingPortalSession(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **createPortalSessionRequest** | [CreatePortalSessionRequest](CreatePortalSessionRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**CreatePortalSessionResponse**](CreatePortalSessionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getCurrentUserUsage

> UserUsageResponse getCurrentUserUsage(authorization, ksUat)

Get Current User Usage Handler

Current user\&#39;s own usage for this period (any authenticated user).

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '@knowledge-stack/ksapi';
import type { GetCurrentUserUsageRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new BillingApi();

  const body = {
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetCurrentUserUsageRequest;

  try {
    const data = await api.getCurrentUserUsage(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**UserUsageResponse**](UserUsageResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getTenantSubscription

> TenantSubscriptionResponse getTenantSubscription(authorization, ksUat)

Get Tenant Subscription Handler

Fetch the tenant\&#39;s current subscription (any authenticated user).

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '@knowledge-stack/ksapi';
import type { GetTenantSubscriptionRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new BillingApi();

  const body = {
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetTenantSubscriptionRequest;

  try {
    const data = await api.getTenantSubscription(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**TenantSubscriptionResponse**](TenantSubscriptionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getTenantUsage

> TenantUsageResponse getTenantUsage(authorization, ksUat)

Get Tenant Usage Handler

Tenant-wide usage (OWNER/ADMIN only).

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '@knowledge-stack/ksapi';
import type { GetTenantUsageRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new BillingApi();

  const body = {
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetTenantUsageRequest;

  try {
    const data = await api.getTenantUsage(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**TenantUsageResponse**](TenantUsageResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listBillingPlans

> Array&lt;BillingPlanResponse&gt; listBillingPlans(authorization, ksUat)

List Billing Plans Handler

List all active plans. Any authenticated user can see the catalog.

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '@knowledge-stack/ksapi';
import type { ListBillingPlansRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new BillingApi();

  const body = {
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies ListBillingPlansRequest;

  try {
    const data = await api.listBillingPlans(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**Array&lt;BillingPlanResponse&gt;**](BillingPlanResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## resumeTenantSubscription

> TenantSubscriptionResponse resumeTenantSubscription(authorization, ksUat)

Resume Tenant Subscription Handler

Undo a prior cancel-at-period-end request.

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '@knowledge-stack/ksapi';
import type { ResumeTenantSubscriptionRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new BillingApi();

  const body = {
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies ResumeTenantSubscriptionRequest;

  try {
    const data = await api.resumeTenantSubscription(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**TenantSubscriptionResponse**](TenantSubscriptionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


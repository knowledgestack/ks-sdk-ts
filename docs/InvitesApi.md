# InvitesApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**acceptInvite**](InvitesApi.md#acceptinvite) | **POST** /v1/invites/{invite_id}/accept | Accept Invite |
| [**createInvite**](InvitesApi.md#createinvite) | **POST** /v1/invites | Create Invite |
| [**deleteInvite**](InvitesApi.md#deleteinvite) | **DELETE** /v1/invites/{invite_id} | Delete Invite |
| [**listInvites**](InvitesApi.md#listinvites) | **GET** /v1/invites | List Invites Handler |



## acceptInvite

> AcceptInviteResponse acceptInvite(inviteId, authorization, ksUat)

Accept Invite

Update an invite to accepted status and create tenant user.

### Example

```ts
import {
  Configuration,
  InvitesApi,
} from '@knowledge-stack/ksapi';
import type { AcceptInviteRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new InvitesApi();

  const body = {
    // string
    inviteId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies AcceptInviteRequest;

  try {
    const data = await api.acceptInvite(body);
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
| **inviteId** | `string` |  | [Defaults to `undefined`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**AcceptInviteResponse**](AcceptInviteResponse.md)

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


## createInvite

> InviteResponse createInvite(inviteUserRequest, authorization, ksUat)

Create Invite

Create an invite for a user to join a tenant (admin-only).  For external IdP tenants (idp_config is set), users are added directly if they exist. For shared IdP tenants (PASSWORD/GOOGLE), an email invite is sent that must be accepted.

### Example

```ts
import {
  Configuration,
  InvitesApi,
} from '@knowledge-stack/ksapi';
import type { CreateInviteRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new InvitesApi();

  const body = {
    // InviteUserRequest
    inviteUserRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies CreateInviteRequest;

  try {
    const data = await api.createInvite(body);
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
| **inviteUserRequest** | [InviteUserRequest](InviteUserRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**InviteResponse**](InviteResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## deleteInvite

> deleteInvite(inviteId, authorization, ksUat)

Delete Invite

Hard-delete an invite (admin/owner only).  Permanently removes the invite. The invite must belong to the caller\&#39;s current tenant.

### Example

```ts
import {
  Configuration,
  InvitesApi,
} from '@knowledge-stack/ksapi';
import type { DeleteInviteRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new InvitesApi();

  const body = {
    // string
    inviteId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies DeleteInviteRequest;

  try {
    const data = await api.deleteInvite(body);
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
| **inviteId** | `string` |  | [Defaults to `undefined`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listInvites

> PaginatedResponseInviteResponse listInvites(email, status, limit, offset, authorization, ksUat)

List Invites Handler

List invites with pagination, filtering, and sorting.  Supports filtering by tenant_id (requires admin access), email, and status. Results can be sorted by created_at, updated_at, expires_at, or accepted_at.

### Example

```ts
import {
  Configuration,
  InvitesApi,
} from '@knowledge-stack/ksapi';
import type { ListInvitesRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new InvitesApi();

  const body = {
    // string | Filter by email (case-insensitive partial match) (optional)
    email: email_example,
    // InviteStatus | Filter by invite status (pending, accepted, expired) (optional)
    status: ...,
    // number | Number of items per page (optional)
    limit: 56,
    // number | Number of items to skip (optional)
    offset: 56,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies ListInvitesRequest;

  try {
    const data = await api.listInvites(body);
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
| **email** | `string` | Filter by email (case-insensitive partial match) | [Optional] [Defaults to `undefined`] |
| **status** | `InviteStatus` | Filter by invite status (pending, accepted, expired) | [Optional] [Defaults to `undefined`] [Enum: pending, accepted, expired] |
| **limit** | `number` | Number of items per page | [Optional] [Defaults to `20`] |
| **offset** | `number` | Number of items to skip | [Optional] [Defaults to `0`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**PaginatedResponseInviteResponse**](PaginatedResponseInviteResponse.md)

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


# AuthApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createPasswordUser**](AuthApi.md#createpassworduseroperation) | **POST** /v1/auth/pw/user | Create Password User Handler |
| [**fanweiDirectorySync**](AuthApi.md#fanweidirectorysync) | **POST** /v1/auth/sso/{tenant_id}/directory_sync | Directory Sync Handler |
| [**fanweiDirectorySync_0**](AuthApi.md#fanweidirectorysync_0) | **POST** /v1/auth/sso/{tenant_id}/directory_sync | Directory Sync Handler |
| [**initiateSso**](AuthApi.md#initiatesso) | **POST** /v1/auth/sso/initiate | Initiate Sso Handler |
| [**oauth2Callback**](AuthApi.md#oauth2callback) | **GET** /v1/auth/sso/oauth2/callback | Oauth2 Callback Handler |
| [**pwEmailVerification**](AuthApi.md#pwemailverification) | **POST** /v1/auth/pw/email_verification | Pw Email Verification Handler |
| [**pwSignin**](AuthApi.md#pwsignin) | **POST** /v1/auth/pw/signin | Signin Handler |
| [**refreshUat**](AuthApi.md#refreshuat) | **POST** /v1/auth/uat | Refresh Uat Handler |
| [**resetPassword**](AuthApi.md#resetpassword) | **POST** /v1/auth/pw/reset | Reset Password Handler |
| [**resetPasswordWithToken**](AuthApi.md#resetpasswordwithtoken) | **POST** /v1/auth/pw/reset_with_token | Reset Password With Token Handler |
| [**sendPwResetEmail**](AuthApi.md#sendpwresetemail) | **POST** /v1/auth/pw/send_reset_email | Send Pw Reset Email Handler |
| [**signout**](AuthApi.md#signout) | **POST** /v1/auth/signout | Signout Handler |
| [**ssoSignin**](AuthApi.md#ssosignin) | **GET** /v1/auth/sso/{tenant_id}/signin | Sso Login Handler |



## createPasswordUser

> UserResponse createPasswordUser(createPasswordUserRequest)

Create Password User Handler

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { CreatePasswordUserOperationRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  const body = {
    // CreatePasswordUserRequest
    createPasswordUserRequest: ...,
  } satisfies CreatePasswordUserOperationRequest;

  try {
    const data = await api.createPasswordUser(body);
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
| **createPasswordUserRequest** | [CreatePasswordUserRequest](CreatePasswordUserRequest.md) |  | |

### Return type

[**UserResponse**](UserResponse.md)

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


## fanweiDirectorySync

> DirectorySyncResponse fanweiDirectorySync(tenantId, authorization, ksUat)

Directory Sync Handler

Trigger directory synchronization for a FanWei E9 tenant.  Accepts either: - A logged-in OWNER/ADMIN user (via UAT cookie) - An admin API key (via Authorization: Bearer header)

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { FanweiDirectorySyncRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  const body = {
    // string
    tenantId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies FanweiDirectorySyncRequest;

  try {
    const data = await api.fanweiDirectorySync(body);
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
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**DirectorySyncResponse**](DirectorySyncResponse.md)

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


## fanweiDirectorySync_0

> DirectorySyncResponse fanweiDirectorySync_0(tenantId, authorization, ksUat)

Directory Sync Handler

Trigger directory synchronization for a FanWei E9 tenant.  Accepts either: - A logged-in OWNER/ADMIN user (via UAT cookie) - An admin API key (via Authorization: Bearer header)

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { FanweiDirectorySync0Request } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  const body = {
    // string
    tenantId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies FanweiDirectorySync0Request;

  try {
    const data = await api.fanweiDirectorySync_0(body);
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
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**DirectorySyncResponse**](DirectorySyncResponse.md)

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


## initiateSso

> SSOInitiateResponse initiateSso(provider, tenantId)

Initiate Sso Handler

Initiate SSO with the given provider and tenant ID.

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { InitiateSsoRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  const body = {
    // IdpType | Provider to initiate SSO with
    provider: ...,
    // string | Tenant ID to initiate SSO with (optional)
    tenantId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies InitiateSsoRequest;

  try {
    const data = await api.initiateSso(body);
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
| **provider** | `IdpType` | Provider to initiate SSO with | [Defaults to `undefined`] [Enum: PASSWORD, GOOGLE, TENANT] |
| **tenantId** | `string` | Tenant ID to initiate SSO with | [Optional] [Defaults to `undefined`] |

### Return type

[**SSOInitiateResponse**](SSOInitiateResponse.md)

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


## oauth2Callback

> UserResponse oauth2Callback(provider, code, state, error, errorDescription, tenantId)

Oauth2 Callback Handler

Handle OAuth2 callback from the given OAuth client.

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { Oauth2CallbackRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  const body = {
    // IdpType | Provider to initiate SSO with
    provider: ...,
    // string | Authorization code from provider (optional)
    code: code_example,
    // string | State parameter for CSRF protection (optional)
    state: state_example,
    // string | Error code if authorization failed (optional)
    error: error_example,
    // string | Error description (optional)
    errorDescription: errorDescription_example,
    // string | Tenant ID to initiate SSO with (optional)
    tenantId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies Oauth2CallbackRequest;

  try {
    const data = await api.oauth2Callback(body);
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
| **provider** | `IdpType` | Provider to initiate SSO with | [Defaults to `undefined`] [Enum: PASSWORD, GOOGLE, TENANT] |
| **code** | `string` | Authorization code from provider | [Optional] [Defaults to `undefined`] |
| **state** | `string` | State parameter for CSRF protection | [Optional] [Defaults to `undefined`] |
| **error** | `string` | Error code if authorization failed | [Optional] [Defaults to `undefined`] |
| **errorDescription** | `string` | Error description | [Optional] [Defaults to `undefined`] |
| **tenantId** | `string` | Tenant ID to initiate SSO with | [Optional] [Defaults to `undefined`] |

### Return type

[**UserResponse**](UserResponse.md)

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


## pwEmailVerification

> EmailSentResponse pwEmailVerification(emailVerificationRequest)

Pw Email Verification Handler

Send password user email verification email.  This endpoint is the first step in the password user creation process. The user receives an email with a link to create their account.

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { PwEmailVerificationRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  const body = {
    // EmailVerificationRequest
    emailVerificationRequest: ...,
  } satisfies PwEmailVerificationRequest;

  try {
    const data = await api.pwEmailVerification(body);
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
| **emailVerificationRequest** | [EmailVerificationRequest](EmailVerificationRequest.md) |  | |

### Return type

[**EmailSentResponse**](EmailSentResponse.md)

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


## pwSignin

> UserResponse pwSignin(signInRequest)

Signin Handler

Validate password credentials and redirect to callback.  This endpoint validates the user\&#39;s credentials and stores the user ID in the session, then redirects to /auth/callback?method&#x3D;pw to maintain consistency with OAuth flows.

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { PwSigninRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  const body = {
    // SignInRequest
    signInRequest: ...,
  } satisfies PwSigninRequest;

  try {
    const data = await api.pwSignin(body);
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
| **signInRequest** | [SignInRequest](SignInRequest.md) |  | |

### Return type

[**UserResponse**](UserResponse.md)

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


## refreshUat

> UserResponse refreshUat(tenantId, authorization, ksUat)

Refresh Uat Handler

Refresh or switch the user\&#39;s active tenant token.

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { RefreshUatRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  const body = {
    // string | Target tenant ID to switch to. None=refresh current tenant (optional)
    tenantId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies RefreshUatRequest;

  try {
    const data = await api.refreshUat(body);
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
| **tenantId** | `string` | Target tenant ID to switch to. None&#x3D;refresh current tenant | [Optional] [Defaults to `undefined`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**UserResponse**](UserResponse.md)

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


## resetPassword

> UserResponse resetPassword(passwordResetRequest, authorization, ksUat)

Reset Password Handler

Reset password for the authenticated user

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { ResetPasswordRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  const body = {
    // PasswordResetRequest
    passwordResetRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies ResetPasswordRequest;

  try {
    const data = await api.resetPassword(body);
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
| **passwordResetRequest** | [PasswordResetRequest](PasswordResetRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**UserResponse**](UserResponse.md)

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


## resetPasswordWithToken

> UserResponse resetPasswordWithToken(passwordResetWithTokenRequest)

Reset Password With Token Handler

Reset password with email verification token

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { ResetPasswordWithTokenRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  const body = {
    // PasswordResetWithTokenRequest
    passwordResetWithTokenRequest: ...,
  } satisfies ResetPasswordWithTokenRequest;

  try {
    const data = await api.resetPasswordWithToken(body);
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
| **passwordResetWithTokenRequest** | [PasswordResetWithTokenRequest](PasswordResetWithTokenRequest.md) |  | |

### Return type

[**UserResponse**](UserResponse.md)

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


## sendPwResetEmail

> EmailSentResponse sendPwResetEmail(emailVerificationRequest)

Send Pw Reset Email Handler

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { SendPwResetEmailRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  const body = {
    // EmailVerificationRequest
    emailVerificationRequest: ...,
  } satisfies SendPwResetEmailRequest;

  try {
    const data = await api.sendPwResetEmail(body);
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
| **emailVerificationRequest** | [EmailVerificationRequest](EmailVerificationRequest.md) |  | |

### Return type

[**EmailSentResponse**](EmailSentResponse.md)

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


## signout

> any signout()

Signout Handler

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { SignoutRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  try {
    const data = await api.signout();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters

This endpoint does not need any parameter.

### Return type

**any**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## ssoSignin

> ssoSignin(tenantId, redirect)

Sso Login Handler

SSO login endpoint.  Resolves the tenant\&#39;s IdP configuration and dispatches to the appropriate provider-specific handler. Sets the UAT cookie and redirects to the frontend.

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@knowledge-stack/ksapi';
import type { SsoSigninRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new AuthApi();

  const body = {
    // string
    tenantId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string | Post-login redirect path (optional)
    redirect: redirect_example,
  } satisfies SsoSigninRequest;

  try {
    const data = await api.ssoSignin(body);
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
| **redirect** | `string` | Post-login redirect path | [Optional] [Defaults to `&#39;&#39;`] |

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
| **307** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


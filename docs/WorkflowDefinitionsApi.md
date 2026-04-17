# WorkflowDefinitionsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createWorkflowDefinition**](WorkflowDefinitionsApi.md#createworkflowdefinitionoperation) | **POST** /v1/workflow-definitions | Create Workflow Definition Handler |
| [**deleteWorkflowDefinition**](WorkflowDefinitionsApi.md#deleteworkflowdefinition) | **DELETE** /v1/workflow-definitions/{definition_id} | Delete Workflow Definition Handler |
| [**getWorkflowDefinition**](WorkflowDefinitionsApi.md#getworkflowdefinition) | **GET** /v1/workflow-definitions/{definition_id} | Get Workflow Definition Handler |
| [**invokeWorkflow**](WorkflowDefinitionsApi.md#invokeworkflowoperation) | **POST** /v1/workflow-definitions/{definition_id}/invoke | Invoke Workflow Handler |
| [**listWorkflowDefinitions**](WorkflowDefinitionsApi.md#listworkflowdefinitions) | **GET** /v1/workflow-definitions | List Workflow Definitions Handler |
| [**listWorkflowRuns**](WorkflowDefinitionsApi.md#listworkflowruns) | **GET** /v1/workflow-definitions/{definition_id}/runs | List Workflow Runs Handler |
| [**updateWorkflowDefinition**](WorkflowDefinitionsApi.md#updateworkflowdefinitionoperation) | **PUT** /v1/workflow-definitions/{definition_id} | Update Workflow Definition Handler |



## createWorkflowDefinition

> WorkflowDefinitionResponse createWorkflowDefinition(createWorkflowDefinitionRequest, authorization, ksUat)

Create Workflow Definition Handler

### Example

```ts
import {
  Configuration,
  WorkflowDefinitionsApi,
} from '@knowledge-stack/ksapi';
import type { CreateWorkflowDefinitionOperationRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new WorkflowDefinitionsApi();

  const body = {
    // CreateWorkflowDefinitionRequest
    createWorkflowDefinitionRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies CreateWorkflowDefinitionOperationRequest;

  try {
    const data = await api.createWorkflowDefinition(body);
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
| **createWorkflowDefinitionRequest** | [CreateWorkflowDefinitionRequest](CreateWorkflowDefinitionRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**WorkflowDefinitionResponse**](WorkflowDefinitionResponse.md)

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


## deleteWorkflowDefinition

> deleteWorkflowDefinition(definitionId, authorization, ksUat)

Delete Workflow Definition Handler

### Example

```ts
import {
  Configuration,
  WorkflowDefinitionsApi,
} from '@knowledge-stack/ksapi';
import type { DeleteWorkflowDefinitionRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new WorkflowDefinitionsApi();

  const body = {
    // string
    definitionId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies DeleteWorkflowDefinitionRequest;

  try {
    const data = await api.deleteWorkflowDefinition(body);
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
| **definitionId** | `string` |  | [Defaults to `undefined`] |
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


## getWorkflowDefinition

> WorkflowDefinitionResponse getWorkflowDefinition(definitionId, authorization, ksUat)

Get Workflow Definition Handler

### Example

```ts
import {
  Configuration,
  WorkflowDefinitionsApi,
} from '@knowledge-stack/ksapi';
import type { GetWorkflowDefinitionRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new WorkflowDefinitionsApi();

  const body = {
    // string
    definitionId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetWorkflowDefinitionRequest;

  try {
    const data = await api.getWorkflowDefinition(body);
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
| **definitionId** | `string` |  | [Defaults to `undefined`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**WorkflowDefinitionResponse**](WorkflowDefinitionResponse.md)

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


## invokeWorkflow

> WorkflowRunResponse invokeWorkflow(definitionId, invokeWorkflowRequest, authorization, ksUat)

Invoke Workflow Handler

### Example

```ts
import {
  Configuration,
  WorkflowDefinitionsApi,
} from '@knowledge-stack/ksapi';
import type { InvokeWorkflowOperationRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new WorkflowDefinitionsApi();

  const body = {
    // string
    definitionId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // InvokeWorkflowRequest
    invokeWorkflowRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies InvokeWorkflowOperationRequest;

  try {
    const data = await api.invokeWorkflow(body);
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
| **definitionId** | `string` |  | [Defaults to `undefined`] |
| **invokeWorkflowRequest** | [InvokeWorkflowRequest](InvokeWorkflowRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**WorkflowRunResponse**](WorkflowRunResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listWorkflowDefinitions

> PaginatedResponseWorkflowDefinitionResponse listWorkflowDefinitions(limit, offset, authorization, ksUat)

List Workflow Definitions Handler

### Example

```ts
import {
  Configuration,
  WorkflowDefinitionsApi,
} from '@knowledge-stack/ksapi';
import type { ListWorkflowDefinitionsRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new WorkflowDefinitionsApi();

  const body = {
    // number | Number of items per page (optional)
    limit: 56,
    // number | Number of items to skip (optional)
    offset: 56,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies ListWorkflowDefinitionsRequest;

  try {
    const data = await api.listWorkflowDefinitions(body);
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
| **limit** | `number` | Number of items per page | [Optional] [Defaults to `20`] |
| **offset** | `number` | Number of items to skip | [Optional] [Defaults to `0`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**PaginatedResponseWorkflowDefinitionResponse**](PaginatedResponseWorkflowDefinitionResponse.md)

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


## listWorkflowRuns

> PaginatedResponseWorkflowRunResponse listWorkflowRuns(definitionId, limit, offset, authorization, ksUat)

List Workflow Runs Handler

### Example

```ts
import {
  Configuration,
  WorkflowDefinitionsApi,
} from '@knowledge-stack/ksapi';
import type { ListWorkflowRunsRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new WorkflowDefinitionsApi();

  const body = {
    // string
    definitionId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // number | Number of items per page (optional)
    limit: 56,
    // number | Number of items to skip (optional)
    offset: 56,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies ListWorkflowRunsRequest;

  try {
    const data = await api.listWorkflowRuns(body);
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
| **definitionId** | `string` |  | [Defaults to `undefined`] |
| **limit** | `number` | Number of items per page | [Optional] [Defaults to `20`] |
| **offset** | `number` | Number of items to skip | [Optional] [Defaults to `0`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**PaginatedResponseWorkflowRunResponse**](PaginatedResponseWorkflowRunResponse.md)

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


## updateWorkflowDefinition

> WorkflowDefinitionResponse updateWorkflowDefinition(definitionId, updateWorkflowDefinitionRequest, authorization, ksUat)

Update Workflow Definition Handler

### Example

```ts
import {
  Configuration,
  WorkflowDefinitionsApi,
} from '@knowledge-stack/ksapi';
import type { UpdateWorkflowDefinitionOperationRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new WorkflowDefinitionsApi();

  const body = {
    // string
    definitionId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpdateWorkflowDefinitionRequest
    updateWorkflowDefinitionRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies UpdateWorkflowDefinitionOperationRequest;

  try {
    const data = await api.updateWorkflowDefinition(body);
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
| **definitionId** | `string` |  | [Defaults to `undefined`] |
| **updateWorkflowDefinitionRequest** | [UpdateWorkflowDefinitionRequest](UpdateWorkflowDefinitionRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**WorkflowDefinitionResponse**](WorkflowDefinitionResponse.md)

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


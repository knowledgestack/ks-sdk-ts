# WorkflowRunsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteWorkflowRun**](WorkflowRunsApi.md#deleteworkflowrun) | **DELETE** /v1/workflow-runs/{run_id} | Delete Workflow Run Handler |
| [**getWorkflowRun**](WorkflowRunsApi.md#getworkflowrun) | **GET** /v1/workflow-runs/{run_id} | Get Workflow Run Handler |
| [**workflowRunCallback**](WorkflowRunsApi.md#workflowruncallbackoperation) | **POST** /v1/workflow-runs/{run_id}/callback | Workflow Run Callback Handler |



## deleteWorkflowRun

> deleteWorkflowRun(runId, authorization, ksUat)

Delete Workflow Run Handler

### Example

```ts
import {
  Configuration,
  WorkflowRunsApi,
} from '@knowledge-stack/ksapi';
import type { DeleteWorkflowRunRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new WorkflowRunsApi();

  const body = {
    // string
    runId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies DeleteWorkflowRunRequest;

  try {
    const data = await api.deleteWorkflowRun(body);
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
| **runId** | `string` |  | [Defaults to `undefined`] |
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


## getWorkflowRun

> WorkflowRunResponse getWorkflowRun(runId, authorization, ksUat)

Get Workflow Run Handler

### Example

```ts
import {
  Configuration,
  WorkflowRunsApi,
} from '@knowledge-stack/ksapi';
import type { GetWorkflowRunRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new WorkflowRunsApi();

  const body = {
    // string
    runId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetWorkflowRunRequest;

  try {
    const data = await api.getWorkflowRun(body);
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
| **runId** | `string` |  | [Defaults to `undefined`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**WorkflowRunResponse**](WorkflowRunResponse.md)

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


## workflowRunCallback

> WorkflowCallbackResponse workflowRunCallback(runId, workflowRunCallbackRequest)

Workflow Run Callback Handler

### Example

```ts
import {
  Configuration,
  WorkflowRunsApi,
} from '@knowledge-stack/ksapi';
import type { WorkflowRunCallbackOperationRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new WorkflowRunsApi();

  const body = {
    // string
    runId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // WorkflowRunCallbackRequest
    workflowRunCallbackRequest: ...,
  } satisfies WorkflowRunCallbackOperationRequest;

  try {
    const data = await api.workflowRunCallback(body);
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
| **runId** | `string` |  | [Defaults to `undefined`] |
| **workflowRunCallbackRequest** | [WorkflowRunCallbackRequest](WorkflowRunCallbackRequest.md) |  | |

### Return type

[**WorkflowCallbackResponse**](WorkflowCallbackResponse.md)

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


# PathPartsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**bulkAddPathPartTags**](PathPartsApi.md#bulkaddpathparttags) | **POST** /v1/path-parts/{path_part_id}/tags | Bulk Add Path Part Tags Handler |
| [**bulkRemovePathPartTags**](PathPartsApi.md#bulkremovepathparttags) | **DELETE** /v1/path-parts/{path_part_id}/tags | Bulk Remove Path Part Tags Handler |
| [**getPathPart**](PathPartsApi.md#getpathpart) | **GET** /v1/path-parts/{path_part_id} | Get Path Part Handler |
| [**getPathPartAncestry**](PathPartsApi.md#getpathpartancestry) | **GET** /v1/path-parts/{path_part_id}/ancestry | Get Path Part Ancestry Handler |
| [**getPathPartSubtreeChunks**](PathPartsApi.md#getpathpartsubtreechunks) | **GET** /v1/path-parts/{path_part_id}/subtree_chunks | Get Path Part Subtree Chunks Handler |
| [**getPathPartTags**](PathPartsApi.md#getpathparttags) | **GET** /v1/path-parts/{path_part_id}/tags | Get Path Part Tags Handler |
| [**listPathParts**](PathPartsApi.md#listpathparts) | **GET** /v1/path-parts | List Path Parts Handler |



## bulkAddPathPartTags

> PathPartTagsResponse bulkAddPathPartTags(pathPartId, bulkTagRequest, authorization, ksUat)

Bulk Add Path Part Tags Handler

Bulk add tags to a path part.  Idempotent — already-attached tags are skipped. Returns 400 if any tag_id doesn\&#39;t exist (FK violation). Requires write permission on the target path part.

### Example

```ts
import {
  Configuration,
  PathPartsApi,
} from '@knowledge-stack/ksapi';
import type { BulkAddPathPartTagsRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new PathPartsApi();

  const body = {
    // string
    pathPartId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // BulkTagRequest
    bulkTagRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies BulkAddPathPartTagsRequest;

  try {
    const data = await api.bulkAddPathPartTags(body);
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
| **pathPartId** | `string` |  | [Defaults to `undefined`] |
| **bulkTagRequest** | [BulkTagRequest](BulkTagRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**PathPartTagsResponse**](PathPartTagsResponse.md)

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


## bulkRemovePathPartTags

> PathPartTagsResponse bulkRemovePathPartTags(pathPartId, bulkTagRequest, authorization, ksUat)

Bulk Remove Path Part Tags Handler

Bulk remove tags from a path part.  Silently ignores tags that aren\&#39;t attached. Requires write permission on the target path part.

### Example

```ts
import {
  Configuration,
  PathPartsApi,
} from '@knowledge-stack/ksapi';
import type { BulkRemovePathPartTagsRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new PathPartsApi();

  const body = {
    // string
    pathPartId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // BulkTagRequest
    bulkTagRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies BulkRemovePathPartTagsRequest;

  try {
    const data = await api.bulkRemovePathPartTags(body);
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
| **pathPartId** | `string` |  | [Defaults to `undefined`] |
| **bulkTagRequest** | [BulkTagRequest](BulkTagRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**PathPartTagsResponse**](PathPartTagsResponse.md)

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


## getPathPart

> PathPartResponse getPathPart(pathPartId, authorization, ksUat)

Get Path Part Handler

Get a path part by its ID.  Returns the path part with its attached tag IDs.

### Example

```ts
import {
  Configuration,
  PathPartsApi,
} from '@knowledge-stack/ksapi';
import type { GetPathPartRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new PathPartsApi();

  const body = {
    // string
    pathPartId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetPathPartRequest;

  try {
    const data = await api.getPathPart(body);
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
| **pathPartId** | `string` |  | [Defaults to `undefined`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**PathPartResponse**](PathPartResponse.md)

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


## getPathPartAncestry

> AncestryResponse getPathPartAncestry(pathPartId, authorization, ksUat)

Get Path Part Ancestry Handler

Get the full ancestry chain for a path part (root to leaf, inclusive).  Returns all ancestors from the root down to and including the target path part. Authorization is checked on the leaf — if the user can read the leaf, they can navigate its ancestors.

### Example

```ts
import {
  Configuration,
  PathPartsApi,
} from '@knowledge-stack/ksapi';
import type { GetPathPartAncestryRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new PathPartsApi();

  const body = {
    // string
    pathPartId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetPathPartAncestryRequest;

  try {
    const data = await api.getPathPartAncestry(body);
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
| **pathPartId** | `string` |  | [Defaults to `undefined`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**AncestryResponse**](AncestryResponse.md)

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


## getPathPartSubtreeChunks

> SubtreeChunksResponse getPathPartSubtreeChunks(pathPartId, authorization, ksUat)

Get Path Part Subtree Chunks Handler

Resolve all descendant chunks for a subtree root.  Returns chunks grouped by identical (path_part_ids, tag_ids) tuples.

### Example

```ts
import {
  Configuration,
  PathPartsApi,
} from '@knowledge-stack/ksapi';
import type { GetPathPartSubtreeChunksRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new PathPartsApi();

  const body = {
    // string
    pathPartId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetPathPartSubtreeChunksRequest;

  try {
    const data = await api.getPathPartSubtreeChunks(body);
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
| **pathPartId** | `string` |  | [Defaults to `undefined`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**SubtreeChunksResponse**](SubtreeChunksResponse.md)

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


## getPathPartTags

> PathPartTagsResponse getPathPartTags(pathPartId, includeInherited, authorization, ksUat)

Get Path Part Tags Handler

Get tags for a path part.  When include_inherited&#x3D;False (default), returns only directly-attached tags. When include_inherited&#x3D;True, walks the ancestor chain and returns the deduplicated union of tags from all ancestors (including the path part itself).

### Example

```ts
import {
  Configuration,
  PathPartsApi,
} from '@knowledge-stack/ksapi';
import type { GetPathPartTagsRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new PathPartsApi();

  const body = {
    // string
    pathPartId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // boolean | Include tags inherited from ancestor path parts (optional)
    includeInherited: true,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetPathPartTagsRequest;

  try {
    const data = await api.getPathPartTags(body);
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
| **pathPartId** | `string` |  | [Defaults to `undefined`] |
| **includeInherited** | `boolean` | Include tags inherited from ancestor path parts | [Optional] [Defaults to `false`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**PathPartTagsResponse**](PathPartTagsResponse.md)

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


## listPathParts

> PaginatedResponsePathPartResponse listPathParts(parentPathId, maxDepth, sortOrder, limit, offset, authorization, ksUat)

List Path Parts Handler

List path parts (folders) under a parent with traversal.  This is a generic endpoint for traversing the folder hierarchy. It returns only FOLDER type path parts.  - If parent_path_id is not provided, lists contents of the root folder. - max_depth controls how deep to traverse (1 &#x3D; direct children only). - sort_order controls the ordering: LOGICAL (linked-list), NAME, UPDATED_AT, CREATED_AT.  For listing folder contents that includes documents with enriched metadata, use GET /folders/{folder_id}/contents instead.

### Example

```ts
import {
  Configuration,
  PathPartsApi,
} from '@knowledge-stack/ksapi';
import type { ListPathPartsRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new PathPartsApi();

  const body = {
    // string | Parent PathPart ID (defaults to root) (optional)
    parentPathId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // number | Maximum depth to traverse (1 = direct children, default: 1) (optional)
    maxDepth: 56,
    // PathOrder | Sort order for results (default: LOGICAL) (optional)
    sortOrder: ...,
    // number | Number of items per page (optional)
    limit: 56,
    // number | Number of items to skip (optional)
    offset: 56,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies ListPathPartsRequest;

  try {
    const data = await api.listPathParts(body);
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
| **parentPathId** | `string` | Parent PathPart ID (defaults to root) | [Optional] [Defaults to `undefined`] |
| **maxDepth** | `number` | Maximum depth to traverse (1 &#x3D; direct children, default: 1) | [Optional] [Defaults to `1`] |
| **sortOrder** | `PathOrder` | Sort order for results (default: LOGICAL) | [Optional] [Defaults to `undefined`] [Enum: LOGICAL, NAME, UPDATED_AT, CREATED_AT] |
| **limit** | `number` | Number of items per page | [Optional] [Defaults to `20`] |
| **offset** | `number` | Number of items to skip | [Optional] [Defaults to `0`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**PaginatedResponsePathPartResponse**](PaginatedResponsePathPartResponse.md)

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


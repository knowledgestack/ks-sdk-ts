# ChunksApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createChunk**](ChunksApi.md#createchunkoperation) | **POST** /v1/chunks | Create Chunk Handler |
| [**deleteChunk**](ChunksApi.md#deletechunk) | **DELETE** /v1/chunks/{chunk_id} | Delete Chunk Handler |
| [**getChunk**](ChunksApi.md#getchunk) | **GET** /v1/chunks/{chunk_id} | Get Chunk Handler |
| [**getChunkNeighbors**](ChunksApi.md#getchunkneighbors) | **GET** /v1/chunks/{chunk_id}/neighbors | Get Chunk Neighbors Handler |
| [**getChunksBulk**](ChunksApi.md#getchunksbulk) | **GET** /v1/chunks/bulk | Get Chunks Bulk Handler |
| [**getVersionChunkIds**](ChunksApi.md#getversionchunkids) | **GET** /v1/chunks/version-chunk-ids | Get Version Chunk Ids Handler |
| [**searchChunks**](ChunksApi.md#searchchunks) | **POST** /v1/chunks/search | Search Chunks Handler |
| [**updateChunkContent**](ChunksApi.md#updatechunkcontentoperation) | **PATCH** /v1/chunks/{chunk_id}/content | Update Chunk Content Handler |
| [**updateChunkMetadata**](ChunksApi.md#updatechunkmetadataoperation) | **PATCH** /v1/chunks/{chunk_id} | Update Chunk Metadata Handler |



## createChunk

> ChunkResponse createChunk(createChunkRequest, authorization, ksUat)

Create Chunk Handler

Create a new chunk with content.  The chunk is created as a child of the specified parent (must be DOCUMENT_VERSION or SECTION). Content is deduplicated by SHA256 hash.

### Example

```ts
import {
  Configuration,
  ChunksApi,
} from '@knowledge-stack/ksapi';
import type { CreateChunkOperationRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new ChunksApi();

  const body = {
    // CreateChunkRequest
    createChunkRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies CreateChunkOperationRequest;

  try {
    const data = await api.createChunk(body);
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
| **createChunkRequest** | [CreateChunkRequest](CreateChunkRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**ChunkResponse**](ChunkResponse.md)

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


## deleteChunk

> deleteChunk(chunkId, authorization, ksUat)

Delete Chunk Handler

Delete a chunk.  The chunk is deleted via its PathPart (cascading delete). The associated ChunkContent may remain if shared by other chunks.

### Example

```ts
import {
  Configuration,
  ChunksApi,
} from '@knowledge-stack/ksapi';
import type { DeleteChunkRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new ChunksApi();

  const body = {
    // string
    chunkId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies DeleteChunkRequest;

  try {
    const data = await api.deleteChunk(body);
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
| **chunkId** | `string` |  | [Defaults to `undefined`] |
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


## getChunk

> ChunkResponse getChunk(chunkId, withDocument, authorization, ksUat)

Get Chunk Handler

Get a chunk by its ID, including content.

### Example

```ts
import {
  Configuration,
  ChunksApi,
} from '@knowledge-stack/ksapi';
import type { GetChunkRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new ChunksApi();

  const body = {
    // string
    chunkId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // boolean | Include ancestor document_id and document_version_id (default: false) (optional)
    withDocument: true,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetChunkRequest;

  try {
    const data = await api.getChunk(body);
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
| **chunkId** | `string` |  | [Defaults to `undefined`] |
| **withDocument** | `boolean` | Include ancestor document_id and document_version_id (default: false) | [Optional] [Defaults to `false`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**ChunkResponse**](ChunkResponse.md)

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


## getChunkNeighbors

> ChunkNeighborsResponse getChunkNeighbors(chunkId, prev, next, chunksOnly, authorization, ksUat)

Get Chunk Neighbors Handler

Get neighboring siblings by traversing the sibling linked list.  Walks the sibling chain backward (prev) and forward (next) from the anchor chunk. Returns sections and chunks in sibling order within the same parent.  When &#x60;&#x60;chunks_only&#x3D;true&#x60;&#x60;, the traversal stops at the first non-CHUNK sibling in each direction, returning only chunk neighbors.

### Example

```ts
import {
  Configuration,
  ChunksApi,
} from '@knowledge-stack/ksapi';
import type { GetChunkNeighborsRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new ChunksApi();

  const body = {
    // string
    chunkId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // number | Number of preceding siblings to include (optional)
    prev: 56,
    // number | Number of succeeding siblings to include (optional)
    next: 56,
    // boolean | When true, stop traversal at non-CHUNK siblings (default: false) (optional)
    chunksOnly: true,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetChunkNeighborsRequest;

  try {
    const data = await api.getChunkNeighbors(body);
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
| **chunkId** | `string` |  | [Defaults to `undefined`] |
| **prev** | `number` | Number of preceding siblings to include | [Optional] [Defaults to `1`] |
| **next** | `number` | Number of succeeding siblings to include | [Optional] [Defaults to `1`] |
| **chunksOnly** | `boolean` | When true, stop traversal at non-CHUNK siblings (default: false) | [Optional] [Defaults to `false`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**ChunkNeighborsResponse**](ChunkNeighborsResponse.md)

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


## getChunksBulk

> Array&lt;ChunkBulkResponse&gt; getChunksBulk(chunkIds, authorization, ksUat)

Get Chunks Bulk Handler

Batch-fetch chunks with their full ancestor path part IDs.  Returns standard chunk data plus path_part_id_segments (the ordered ancestor chain from root to chunk) for each requested chunk. Non-existent IDs are silently skipped. Limited to 200 IDs per call.

### Example

```ts
import {
  Configuration,
  ChunksApi,
} from '@knowledge-stack/ksapi';
import type { GetChunksBulkRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new ChunksApi();

  const body = {
    // Array<string> | Chunk IDs to resolve (max 200) (optional)
    chunkIds: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetChunksBulkRequest;

  try {
    const data = await api.getChunksBulk(body);
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
| **chunkIds** | `Array<string>` | Chunk IDs to resolve (max 200) | [Optional] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**Array&lt;ChunkBulkResponse&gt;**](ChunkBulkResponse.md)

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


## getVersionChunkIds

> VersionChunkIdsResponse getVersionChunkIds(documentVersionId, authorization, ksUat)

Get Version Chunk Ids Handler

Get all chunk IDs belonging to a document version.  Used by the embedding pipeline to discover chunks for a version.

### Example

```ts
import {
  Configuration,
  ChunksApi,
} from '@knowledge-stack/ksapi';
import type { GetVersionChunkIdsRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new ChunksApi();

  const body = {
    // string | Document version ID
    documentVersionId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies GetVersionChunkIdsRequest;

  try {
    const data = await api.getVersionChunkIds(body);
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
| **documentVersionId** | `string` | Document version ID | [Defaults to `undefined`] |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**VersionChunkIdsResponse**](VersionChunkIdsResponse.md)

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


## searchChunks

> Array&lt;ScoredChunkResponse&gt; searchChunks(chunkSearchRequest, authorization, ksUat)

Search Chunks Handler

Search over chunks using dense vector similarity or BM25 full-text.  Combines vector/keyword search with path-based authorization and optional metadata filters. Uses Qdrant for search and hydrates results from Postgres.

### Example

```ts
import {
  Configuration,
  ChunksApi,
} from '@knowledge-stack/ksapi';
import type { SearchChunksRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new ChunksApi();

  const body = {
    // ChunkSearchRequest
    chunkSearchRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies SearchChunksRequest;

  try {
    const data = await api.searchChunks(body);
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
| **chunkSearchRequest** | [ChunkSearchRequest](ChunkSearchRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**Array&lt;ScoredChunkResponse&gt;**](ScoredChunkResponse.md)

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


## updateChunkContent

> ChunkResponse updateChunkContent(chunkId, updateChunkContentRequest, authorization, ksUat)

Update Chunk Content Handler

Update chunk content by creating a new content row.  The old content row is preserved (not deleted). If the new content matches an existing content hash, it will be deduplicated.

### Example

```ts
import {
  Configuration,
  ChunksApi,
} from '@knowledge-stack/ksapi';
import type { UpdateChunkContentOperationRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new ChunksApi();

  const body = {
    // string
    chunkId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpdateChunkContentRequest
    updateChunkContentRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies UpdateChunkContentOperationRequest;

  try {
    const data = await api.updateChunkContent(body);
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
| **chunkId** | `string` |  | [Defaults to `undefined`] |
| **updateChunkContentRequest** | [UpdateChunkContentRequest](UpdateChunkContentRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**ChunkResponse**](ChunkResponse.md)

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


## updateChunkMetadata

> ChunkResponse updateChunkMetadata(chunkId, updateChunkMetadataRequest, authorization, ksUat)

Update Chunk Metadata Handler

Update chunk metadata and/or move the chunk.  The provided metadata is shallow-merged into the existing chunk_metadata. Move params (parent_path_part_id, prev_sibling_path_id, move_to_head) allow reparenting or reordering the chunk within the same document version.

### Example

```ts
import {
  Configuration,
  ChunksApi,
} from '@knowledge-stack/ksapi';
import type { UpdateChunkMetadataOperationRequest } from '@knowledge-stack/ksapi';

async function example() {
  console.log("🚀 Testing @knowledge-stack/ksapi SDK...");
  const api = new ChunksApi();

  const body = {
    // string
    chunkId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpdateChunkMetadataRequest
    updateChunkMetadataRequest: ...,
    // string (optional)
    authorization: authorization_example,
    // string (optional)
    ksUat: ksUat_example,
  } satisfies UpdateChunkMetadataOperationRequest;

  try {
    const data = await api.updateChunkMetadata(body);
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
| **chunkId** | `string` |  | [Defaults to `undefined`] |
| **updateChunkMetadataRequest** | [UpdateChunkMetadataRequest](UpdateChunkMetadataRequest.md) |  | |
| **authorization** | `string` |  | [Optional] [Defaults to `undefined`] |
| **ksUat** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**ChunkResponse**](ChunkResponse.md)

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


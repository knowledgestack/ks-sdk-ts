
# TenantUsageResponse

Tenant-wide usage for the current billing period.

## Properties

Name | Type
------------ | -------------
`periodStart` | Date
`periodEnd` | Date
`tokensUsed` | number
`tokensLimit` | number
`documentsProcessed` | number
`documentsLimit` | number
`percentTokensUsed` | number
`percentDocumentsUsed` | number
`isCustomLimit` | boolean

## Example

```typescript
import type { TenantUsageResponse } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "periodStart": null,
  "periodEnd": null,
  "tokensUsed": null,
  "tokensLimit": null,
  "documentsProcessed": null,
  "documentsLimit": null,
  "percentTokensUsed": null,
  "percentDocumentsUsed": null,
  "isCustomLimit": null,
} satisfies TenantUsageResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as TenantUsageResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)



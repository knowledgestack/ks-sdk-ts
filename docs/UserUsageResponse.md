
# UserUsageResponse

Per-user usage snapshot.

## Properties

Name | Type
------------ | -------------
`userId` | string
`periodStart` | Date
`periodEnd` | Date
`tokensUsedThisPeriod` | number
`documentsProcessedThisPeriod` | number

## Example

```typescript
import type { UserUsageResponse } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "userId": null,
  "periodStart": null,
  "periodEnd": null,
  "tokensUsedThisPeriod": null,
  "documentsProcessedThisPeriod": null,
} satisfies UserUsageResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UserUsageResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)



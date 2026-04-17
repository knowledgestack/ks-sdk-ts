
# UpdateDocumentRequest

Request to update a document (rename, move, and/or change active version).

## Properties

Name | Type
------------ | -------------
`name` | string
`parentPathPartId` | string
`activeVersionId` | string

## Example

```typescript
import type { UpdateDocumentRequest } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "name": null,
  "parentPathPartId": null,
  "activeVersionId": null,
} satisfies UpdateDocumentRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UpdateDocumentRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)



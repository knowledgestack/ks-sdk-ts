
# WorkflowDefinitionResponse

Workflow definition response.

## Properties

Name | Type
------------ | -------------
`id` | string
`name` | string
`description` | string
`runnerType` | [WorkflowRunnerType](WorkflowRunnerType.md)
`runnerConfig` | [SelfHostedRunnerConfigResponse](SelfHostedRunnerConfigResponse.md)
`maxRunDurationSeconds` | number
`sourcePathPartIds` | Array&lt;string&gt;
`instructionPathPartIds` | Array&lt;string&gt;
`outputPathPartIds` | Array&lt;string&gt;
`templatePathPartId` | string
`isActive` | boolean
`createdAt` | Date
`updatedAt` | Date

## Example

```typescript
import type { WorkflowDefinitionResponse } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "name": null,
  "description": null,
  "runnerType": null,
  "runnerConfig": null,
  "maxRunDurationSeconds": null,
  "sourcePathPartIds": null,
  "instructionPathPartIds": null,
  "outputPathPartIds": null,
  "templatePathPartId": null,
  "isActive": null,
  "createdAt": null,
  "updatedAt": null,
} satisfies WorkflowDefinitionResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as WorkflowDefinitionResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)




# WorkflowRunResponse

Workflow run response.

## Properties

Name | Type
------------ | -------------
`id` | string
`workflowDefinitionId` | string
`userId` | string
`runnerType` | [WorkflowRunnerType](WorkflowRunnerType.md)
`status` | [WorkflowRunStatus](WorkflowRunStatus.md)
`startedAt` | Date
`completedAt` | Date
`runSnapshot` | [WorkflowRunSnapshot](WorkflowRunSnapshot.md)
`error` | string
`createdAt` | Date
`updatedAt` | Date

## Example

```typescript
import type { WorkflowRunResponse } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "workflowDefinitionId": null,
  "userId": null,
  "runnerType": null,
  "status": null,
  "startedAt": null,
  "completedAt": null,
  "runSnapshot": null,
  "error": null,
  "createdAt": null,
  "updatedAt": null,
} satisfies WorkflowRunResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as WorkflowRunResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)



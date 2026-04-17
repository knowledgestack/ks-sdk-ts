
# WorkflowRunSnapshot

Frozen ABCD configuration captured at workflow trigger time.

## Properties

Name | Type
------------ | -------------
`workflowDefinitionId` | string
`workflowName` | string
`runnerType` | [WorkflowRunnerType](WorkflowRunnerType.md)
`userId` | string
`maxRunDurationSeconds` | number
`sources` | [Array&lt;ABCDPathSnapshot&gt;](ABCDPathSnapshot.md)
`instructions` | [Array&lt;ABCDPathSnapshot&gt;](ABCDPathSnapshot.md)
`outputs` | [Array&lt;ABCDPathSnapshot&gt;](ABCDPathSnapshot.md)
`template` | [ABCDPathSnapshot](ABCDPathSnapshot.md)

## Example

```typescript
import type { WorkflowRunSnapshot } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "workflowDefinitionId": null,
  "workflowName": null,
  "runnerType": null,
  "userId": null,
  "maxRunDurationSeconds": null,
  "sources": null,
  "instructions": null,
  "outputs": null,
  "template": null,
} satisfies WorkflowRunSnapshot

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as WorkflowRunSnapshot
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)



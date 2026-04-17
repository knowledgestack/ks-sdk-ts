
# CreateWorkflowDefinitionRequest

Create a new workflow definition.

## Properties

Name | Type
------------ | -------------
`name` | string
`description` | string
`runnerType` | [WorkflowRunnerType](WorkflowRunnerType.md)
`runnerConfig` | [SelfHostedRunnerConfig](SelfHostedRunnerConfig.md)
`maxRunDurationSeconds` | number
`sourcePathPartIds` | Array&lt;string&gt;
`instructionPathPartIds` | Array&lt;string&gt;
`outputPathPartIds` | Array&lt;string&gt;
`templatePathPartId` | string

## Example

```typescript
import type { CreateWorkflowDefinitionRequest } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "name": null,
  "description": null,
  "runnerType": null,
  "runnerConfig": null,
  "maxRunDurationSeconds": null,
  "sourcePathPartIds": null,
  "instructionPathPartIds": null,
  "outputPathPartIds": null,
  "templatePathPartId": null,
} satisfies CreateWorkflowDefinitionRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateWorkflowDefinitionRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)



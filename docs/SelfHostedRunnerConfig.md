
# SelfHostedRunnerConfig

Configuration for self-hosted workflow runner.

## Properties

Name | Type
------------ | -------------
`url` | string
`webhookSecret` | string

## Example

```typescript
import type { SelfHostedRunnerConfig } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "url": null,
  "webhookSecret": null,
} satisfies SelfHostedRunnerConfig

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as SelfHostedRunnerConfig
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)



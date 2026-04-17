
# CreateCheckoutSessionRequest


## Properties

Name | Type
------------ | -------------
`targetTier` | [BillingPlanTier](BillingPlanTier.md)
`cadence` | [BillingCadence](BillingCadence.md)
`seats` | number
`successUrl` | string
`cancelUrl` | string

## Example

```typescript
import type { CreateCheckoutSessionRequest } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "targetTier": null,
  "cadence": null,
  "seats": null,
  "successUrl": null,
  "cancelUrl": null,
} satisfies CreateCheckoutSessionRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateCheckoutSessionRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)




# TenantSubscriptionResponse

A tenant\'s current subscription.

## Properties

Name | Type
------------ | -------------
`id` | string
`plan` | [BillingPlanResponse](BillingPlanResponse.md)
`status` | [SubscriptionStatus](SubscriptionStatus.md)
`cadence` | [BillingCadence](BillingCadence.md)
`seats` | number
`currentPeriodStart` | Date
`currentPeriodEnd` | Date
`cancelAtPeriodEnd` | boolean
`canceledAt` | Date
`effectiveLimits` | [EffectiveLimitsResponse](EffectiveLimitsResponse.md)
`overrideNotes` | string

## Example

```typescript
import type { TenantSubscriptionResponse } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "plan": null,
  "status": null,
  "cadence": null,
  "seats": null,
  "currentPeriodStart": null,
  "currentPeriodEnd": null,
  "cancelAtPeriodEnd": null,
  "canceledAt": null,
  "effectiveLimits": null,
  "overrideNotes": null,
} satisfies TenantSubscriptionResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as TenantSubscriptionResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)




# EffectiveLimitsResponse

Resolved limits for a tenant (plan defaults + overrides).

## Properties

Name | Type
------------ | -------------
`pricePerSeatCentsMonthly` | number
`pricePerSeatCentsBilled` | number
`monthlyTokenLimit` | number
`monthlyDocumentLimit` | number
`maxSeats` | number
`litellmBudgetCentsPerUser` | number
`hasCustomOverrides` | boolean

## Example

```typescript
import type { EffectiveLimitsResponse } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "pricePerSeatCentsMonthly": null,
  "pricePerSeatCentsBilled": null,
  "monthlyTokenLimit": null,
  "monthlyDocumentLimit": null,
  "maxSeats": null,
  "litellmBudgetCentsPerUser": null,
  "hasCustomOverrides": null,
} satisfies EffectiveLimitsResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as EffectiveLimitsResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)



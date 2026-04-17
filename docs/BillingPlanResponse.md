
# BillingPlanResponse

A plan in the catalog.

## Properties

Name | Type
------------ | -------------
`id` | string
`tier` | [BillingPlanTier](BillingPlanTier.md)
`displayName` | string
`description` | string
`monthlyPricePerSeatCents` | number
`annualPricePerSeatCents` | number
`annualDiscountPercent` | number
`maxSeats` | number
`monthlyTokenLimit` | number
`monthlyDocumentLimit` | number
`litellmBudgetCentsPerUser` | number
`sortOrder` | number

## Example

```typescript
import type { BillingPlanResponse } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "tier": null,
  "displayName": null,
  "description": null,
  "monthlyPricePerSeatCents": null,
  "annualPricePerSeatCents": null,
  "annualDiscountPercent": null,
  "maxSeats": null,
  "monthlyTokenLimit": null,
  "monthlyDocumentLimit": null,
  "litellmBudgetCentsPerUser": null,
  "sortOrder": null,
} satisfies BillingPlanResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as BillingPlanResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)



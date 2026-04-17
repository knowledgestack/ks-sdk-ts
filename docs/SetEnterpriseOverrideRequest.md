
# SetEnterpriseOverrideRequest

Platform-admin-only. Pass ``null`` in any field to leave it unchanged.  Use ``DELETE`` endpoint to clear all overrides.

## Properties

Name | Type
------------ | -------------
`overridePricePerSeatCents` | number
`overrideMonthlyTokenLimit` | number
`overrideMonthlyDocumentLimit` | number
`overrideMaxSeats` | number
`overrideLitellmBudgetCentsPerUser` | number
`overrideNotes` | string

## Example

```typescript
import type { SetEnterpriseOverrideRequest } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "overridePricePerSeatCents": null,
  "overrideMonthlyTokenLimit": null,
  "overrideMonthlyDocumentLimit": null,
  "overrideMaxSeats": null,
  "overrideLitellmBudgetCentsPerUser": null,
  "overrideNotes": null,
} satisfies SetEnterpriseOverrideRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as SetEnterpriseOverrideRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)



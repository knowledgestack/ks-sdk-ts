
# SubscriptionStatus

Tenant subscription lifecycle state, mirrors Stripe subscription status.  Must include every status value Stripe can send, otherwise webhook handling silently drops updates. See https://stripe.com/docs/api/subscriptions/object#subscription_object-status.

## Properties

Name | Type
------------ | -------------

## Example

```typescript
import type { SubscriptionStatus } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
} satisfies SubscriptionStatus

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as SubscriptionStatus
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)



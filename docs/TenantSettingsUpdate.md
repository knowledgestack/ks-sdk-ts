
# TenantSettingsUpdate

Partial tenant settings update.

## Properties

Name | Type
------------ | -------------
`language` | [SupportedLanguage](SupportedLanguage.md)
`description` | string
`timezone` | string
`brandName` | string
`brandColor` | string
`themeOverrides` | { [key: string]: string; }

## Example

```typescript
import type { TenantSettingsUpdate } from '@knowledge-stack/ksapi'

// TODO: Update the object below with actual values
const example = {
  "language": null,
  "description": null,
  "timezone": null,
  "brandName": null,
  "brandColor": null,
  "themeOverrides": null,
} satisfies TenantSettingsUpdate

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as TenantSettingsUpdate
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)



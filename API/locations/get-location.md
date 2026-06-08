# Get location information

| Property | Value |
|-----------|--------|
| **Method** | `GET` |
| **Path** | `/locations/{locationId}` |
| **Category** | Locations |

## Description

Get information about a specific location.

## Parameters

| Name | Type | Location | Required | Description |
|-----|------|-------------|:------:|-------------|
| `locationId` | `string` | path | Yes | Location identifier. |

## Responses

### 200 — Success

```
Location{
localizedName string
id integer
name string
isCountry boolean
countryCode string
}
```

### Standard errors

| Code | Description |
|------|-------------|
| `400` | Client provided incorrect parameters for the request. |
| `403` | Access denied: missing/incorrect credentials or API token lacks access to the resource. |
| `404` | Resource not found. |
| `429` | Request throttled: too many requests for the API token used. |
| `500` | Unknown error while handling the request. |
| `503` | Service temporarily unavailable (maintenance). |

Error format:

```json
{
  "reason": "string",
  "message": "string",
  "type": "string",
  "detail": {}
}
```

[← Back to index](../../README.md)

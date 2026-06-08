# List clan labels

| Property | Value |
|-----------|--------|
| **Method** | `GET` |
| **Path** | `/labels/clans` |
| **Category** | Labels |

## Description

List of available clan labels.

## Parameters

| Name | Type | Location | Required | Description |
|-----|------|-------------|:------:|-------------|
| `limit` | `integer` | query | No | Limit the number of items returned in the response. |
| `after` | `string` | query | No | Items after this marker (in `paging`, field `after`). `after` and `before` are mutually exclusive. |
| `before` | `string` | query | No | Items before this marker (in `paging`, field `before`). `after` and `before` are mutually exclusive. |

## Responses

### 200 — Success

```
LabelList[Label{...}]
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

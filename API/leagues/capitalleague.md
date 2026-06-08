# Get capital league information

| Property | Value |
|-----------|--------|
| **Method** | `GET` |
| **Path** | `/capitalleagues/{leagueId}` |
| **Category** | Leagues |

## Description

Get capital league information

## Parameters

| Name | Type | Location | Required | Description |
|-----|------|-------------|:------:|-------------|
| `leagueId` | `string` | path | Yes | League identifier. |

## Responses

### 200 — Success

```
CapitalLeague{
name JsonLocalizedName{...}
id integer
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

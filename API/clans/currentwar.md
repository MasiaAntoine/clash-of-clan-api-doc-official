# Get clan's current war

| Property | Value |
|-----------|--------|
| **Method** | `GET` |
| **Path** | `/clans/{clanTag}/currentwar` |
| **Category** | Clans |

## Description

Get clan's current war

## Parameters

| Name | Type | Location | Required | Description |
|-----|------|-------------|:------:|-------------|
| `clanTag` | `string` | path | Yes | Tag of the clan. |

## Responses

### 200 — Success

```
ClanWar{
clan WarClan{...}
teamSize integer
attacksPerMember integer
battleModifier stringEnum:
Array [ 2 ]
opponent WarClan{...}
startTime string
state stringEnum:
Array [ 10 ]
endTime string
preparationStartTime string
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

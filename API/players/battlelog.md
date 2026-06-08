# Get player battle log

| Property | Value |
|-----------|--------|
| **Method** | `GET` |
| **Path** | `/players/{playerTag}/battlelog` |
| **Category** | Joueurs |

## Description

Get the player's battle log for recent battles.

## Parameters

| Name | Type | Location | Required | Description |
|-----|------|-------------|:------:|-------------|
| `playerTag` | `string` | path | Yes | Tag of the player. |

## Responses

### 200 — Success

```
BattleLogEntryList[BattleLogEntry{...}]
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

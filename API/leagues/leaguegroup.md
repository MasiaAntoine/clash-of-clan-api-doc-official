# Get ranked battle league group information

| Property | Value |
|-----------|--------|
| **Method** | `GET` |
| **Path** | `/leaguegroup/{leagueGroupTag}/{leagueSeasonId}` |
| **Category** | Leagues |

## Description

Get ranked battle league group information

## Parameters

| Name | Type | Location | Required | Description |
|-----|------|-------------|:------:|-------------|
| `leagueGroupTag` | `string` | path | Yes | League group identifier. |
| `leagueSeasonId` | `string` | path | Yes | League season identifier. |
| `playerTag` | `string` | query | Yes | Tag of the player |

## Responses

### 200 — Success

```
LeagueGroup{
members LeagueGroupMemberList[...]
attackLogs LeagueGroupBattleLogEntryList[...]
defenseLogs LeagueGroupBattleLogEntryList[...]
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

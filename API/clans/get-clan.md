# Get clan information

| Property | Value |
|-----------|--------|
| **Method** | `GET` |
| **Path** | `/clans/{clanTag}` |
| **Category** | Clans |

## Description

Get clan information by tag (via clan search). Tags start with `#` and must be URL-encoded (`#2ABC` → `%232ABC`).

## Parameters

| Name | Type | Location | Required | Description |
|-----|------|-------------|:------:|-------------|
| `clanTag` | `string` | path | Yes | Tag of the clan. |

## Responses

### 200 — Success

```
Clan{
memberList ClanMemberList[...]
warLeague WarLeague{...}
capitalLeague CapitalLeague{...}
tag string
clanBuilderBasePoints integer
clanCapitalPoints integer
requiredTrophies integer
requiredBuilderBaseTrophies integer
requiredTownhallLevel integer
warFrequency stringEnum:
Array [ 7 ]
clanLevel integer
warWinStreak integer
warWins integer
warTies integer
warLosses integer
clanPoints integer
isFamilyFriendly boolean
isWarLogPublic boolean
chatLanguage Language{...}
labels LabelList[...]
name string
location Location{...}
type stringEnum:
Array [ 3 ]
members integer
description string
clanCapital ClanCapital{...}
badgeUrls {...}
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

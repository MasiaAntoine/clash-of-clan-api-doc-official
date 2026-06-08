# Search clans

| Property | Value |
|-----------|--------|
| **Method** | `GET` |
| **Path** | `/clans` |
| **Category** | Clans |

## Description

Search clans by name and/or filter results using various criteria. At least one filter is required. Names must be at least 3 characters. Result ordering is not guaranteed.

## Parameters

| Name | Type | Location | Required | Description |
|-----|------|-------------|:------:|-------------|
| `name` | `string` | query | No | Search by name (min. 3 characters), wildcard allowed. |
| `warFrequency` | `string` | query | No | Filter by war frequency |
| `locationId` | `integer` | query | No | Filter by location (see `GET /locations`). |
| `minMembers` | `integer` | query | No | Minimum number of members |
| `maxMembers` | `integer` | query | No | Maximum number of members |
| `minClanPoints` | `integer` | query | No | Minimum clan points. |
| `minClanLevel` | `integer` | query | No | Minimum clan level. |
| `limit` | `integer` | query | No | Limit the number of items returned in the response. |
| `after` | `string` | query | No | Items after this marker (in `paging`, field `after`). `after` and `before` are mutually exclusive. |
| `before` | `string` | query | No | Items before this marker (in `paging`, field `before`). `after` and `before` are mutually exclusive. |
| `labelIds` | `string` | query | No | Comma-separated label IDs. |

## Responses

### 200 — Success

```
ClanList[Clan{...}]
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

# Verify player API token

| Property | Value |
|-----------|--------|
| **Method** | `POST` |
| **Path** | `/players/{playerTag}/verifytoken` |
| **Category** | Joueurs |

## Description

Verify the one-time API token from in-game settings to confirm account ownership.

## Parameters

| Name | Type | Location | Required | Description |
|-----|------|-------------|:------:|-------------|
| `playerTag` | `string` | path | Yes | Tag of the player. |
| `body` | `object` | body | Yes | JSON request body. |

## Request body

```json
{
"token": "string"
}
```

## Responses

### 200 — Success

```
VerifyTokenResponse{
tag string
token string
status string
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

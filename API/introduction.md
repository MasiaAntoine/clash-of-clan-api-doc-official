# Introduction and authentication

## Quick start

1. Create an account on the [developer portal](https://developer.clashofclans.com).
2. Generate an API token (**My Account**).
3. Add it to every request:

```http
GET /v1/players/%232ABC HTTP/1.1
Host: api.clashofclans.com
Authorization: Bearer YOUR_TOKEN
Accept: application/json
```

## Tag encoding

| In-game | In URL |
|---------|--------|
| `#2ABC` | `%232ABC` |
| `#9G9QGJ2C` | `%239G9QGJ2C` |

## Rate limits and errors

- **429**: too many requests for your token.
- **403**: invalid token or access denied to the resource.
- Responses use `application/json`.

## Pagination

```json
{
  "items": [],
  "paging": {
    "after": "marker_after",
    "before": "marker_before"
  }
}
```

[← Back to index](../README.md)

# Get player information

| Property | Value |
|-----------|--------|
| **Method** | `GET` |
| **Path** | `/players/{playerTag}` |
| **Category** | Joueurs |

## Description

Get player information by tag. Tags are found in-game or in clan member lists. URL-encode `#` as `%23`.

## Parameters

| Name | Type | Location | Required | Description |
|-----|------|-------------|:------:|-------------|
| `playerTag` | `string` | path | Yes | Tag of the player. |

## Responses

### 200 — Success

```
Player{
clan PlayerClan{...}
league League{...}
leagueTier LeagueTier{...}
builderBaseLeague BuilderBaseLeague{...}
role stringEnum:
Array [ 5 ]
warPreference stringEnum:
Array [ 2 ]
attackWins integer
defenseWins integer
townHallLevel integer
townHallWeaponLevel integer
legendStatistics PlayerLegendStatistics{...}
troops PlayerItemLevelList[...]
heroes PlayerItemLevelList[...]
heroEquipment PlayerItemLevelList[...]
spells PlayerItemLevelList[...]
labels LabelList[...]
tag string
name string
expLevel integer
trophies integer
bestTrophies integer
donations integer
donationsReceived integer
builderHallLevel integer
builderBaseTrophies integer
bestBuilderBaseTrophies integer
warStars integer
achievements PlayerAchievementProgressList[...]
clanCapitalContributions integer
playerHouse PlayerHouse{...}
currentLeagueGroupTag string
currentLeagueSeasonId Long{...}
previousLeagueGroupTag string
previousLeagueSeasonId Long{...}
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

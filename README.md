# Clash of Clans API Documentation

Official Clash of Clans API documentation, structured in English.

## Overview

The Clash of Clans API exposes game data in **JSON** format: clans, players,
leagues, locations, rankings, gold pass, and labels.

- [Introduction and authentication](API/introduction.md)
- [Data models](MODELES/README.md)

## Authentication

Every request requires a JWT token in the HTTP header:

```http
Authorization: Bearer YOUR_API_TOKEN
```

Create your token on the **My Account** page of the [Supercell developer portal](https://developer.clashofclans.com).

## Base URL

```
https://api.clashofclans.com/v1
```

> Tags (`#2ABC`) must be URL-encoded (`%232ABC`).

## Routes

### Clans

Access clan-specific information.

- [GET `/clans/{clanTag}/currentwar/leaguegroup`](API/clans/currentwar-leaguegroup.md) — Get clan's current clan war league group
- [GET `/clans/{clanTag}/warlog`](API/clans/warlog.md) — Get clan war log
- [GET `/clans`](API/clans/search.md) — Search clans
- [GET `/clans/{clanTag}/currentwar`](API/clans/currentwar.md) — Get clan's current war
- [GET `/clans/{clanTag}`](API/clans/get-clan.md) — Get clan information
- [GET `/clans/{clanTag}/members`](API/clans/members.md) — List clan members
- [GET `/clans/{clanTag}/capitalraidseasons`](API/clans/capitalraidseasons.md) — Get clan capital raid seasons

### War leagues

Routes related to clan war leagues.

- [GET `/clanwarleagues/wars/{warTag}`](API/clanwarleagues/wars.md) — Get individual clan war league war

### Players

Access player-specific information.

- [GET `/players/{playerTag}`](API/players/get-player.md) — Get player information
- [GET `/players/{playerTag}/battlelog`](API/players/battlelog.md) — Get player battle log
- [POST `/players/{playerTag}/verifytoken`](API/players/verifytoken.md) — Verify player API token
- [GET `/players/{playerTag}/leaguehistory`](API/players/leaguehistory.md) — Get player league history

### Leagues

Access league information.

- [GET `/leaguetiers/{leagueTierId}`](API/leagues/leaguetier.md) — Get league tier information
- [GET `/capitalleagues`](API/leagues/capitalleagues.md) — List capital leagues
- [GET `/leaguetiers`](API/leagues/leaguetiers.md) — List league tiers
- [GET `/leagues`](API/leagues/list.md) — List leagues
- [GET `/leagues/{leagueId}/seasons/{seasonId}`](API/leagues/season.md) — Get league season rankings
- [GET `/capitalleagues/{leagueId}`](API/leagues/capitalleague.md) — Get capital league information
- [GET `/builderbaseleagues/{leagueId}`](API/leagues/builderbaseleague.md) — Get Builder Base league information
- [GET `/builderbaseleagues`](API/leagues/builderbaseleagues.md) — List Builder Base leagues
- [GET `/leagues/{leagueId}`](API/leagues/league.md) — Get league information
- [GET `/leaguegroup/{leagueGroupTag}/{leagueSeasonId}`](API/leagues/leaguegroup.md) — Get ranked battle league group information
- [GET `/leagues/{leagueId}/seasons`](API/leagues/seasons.md) — Get league seasons
- [GET `/warleagues/{leagueId}`](API/leagues/warleague.md) — Get war league information
- [GET `/warleagues`](API/leagues/warleagues.md) — List war leagues

### Locations

Access global and local rankings.

- [GET `/locations/{locationId}/rankings/clans`](API/locations/rankings-clans.md) — Get clan rankings for a location
- [GET `/locations/{locationId}/rankings/players`](API/locations/rankings-players.md) — Get player rankings for a location
- [GET `/locations/{locationId}/rankings/players-builder-base`](API/locations/rankings-players-builder-base.md) — Get Builder Base player rankings for a location
- [GET `/locations/{locationId}/rankings/clans-builder-base`](API/locations/rankings-clans-builder-base.md) — Get Builder Base clan rankings for a location
- [GET `/locations`](API/locations/list.md) — List locations
- [GET `/locations/{locationId}/rankings/capitals`](API/locations/rankings-capitals.md) — Get capital rankings for a location
- [GET `/locations/{locationId}`](API/locations/get-location.md) — Get location information

### Gold pass

Gold pass information.

- [GET `/goldpass/seasons/current`](API/goldpass/seasons-current.md) — Get current gold pass season

### Labels

List clan and player labels.

- [GET `/labels/players`](API/labels/players.md) — List player labels
- [GET `/labels/clans`](API/labels/clans.md) — List clan labels

## Pagination

Lists accept `limit`, `after`, and `before`. Pagination markers are in `paging`.
Use `after` **or** `before`, never both.

## Terms of use

Subject to [Supercell terms](https://developer.clashofclans.com).

# `PlayerLegendStatistics`

**Category:** Players

## Schema

```
PlayerLegendStatistics{
  currentSeason LegendLeagueTournamentSeasonResult{
    trophies integer
    id string
    rank integer
  }
  bestSeason LegendLeagueTournamentSeasonResult{
    trophies integer
    id string
    rank integer
  }
  legendTrophies integer
  previousSeason LegendLeagueTournamentSeasonResult{
    trophies integer
    id string
    rank integer
  }
  previousBuilderBaseSeason LegendLeagueTournamentSeasonResult{
    trophies integer
    id string
    rank integer
  }
  bestBuilderBaseSeason LegendLeagueTournamentSeasonResult{
    trophies integer
    id string
    rank integer
  }
}
```

[← Models index](../README.md) · [← API documentation](../../README.md)

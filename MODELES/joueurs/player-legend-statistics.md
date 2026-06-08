# `PlayerLegendStatistics`

**Catégorie :** Joueurs

## Schéma

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

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

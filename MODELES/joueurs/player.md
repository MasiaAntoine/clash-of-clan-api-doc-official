# `Player`

**Catégorie :** Joueurs

## Schéma

```
Player{
  clan PlayerClan{
    tag string
    clanLevel integer
    name string
    badgeUrls {
    }
  }
  league League{
    name JsonLocalizedName{
    }
    id integer
    iconUrls {
    }
  }
  leagueTier LeagueTier{
    name JsonLocalizedName{
    }
    id integer
    iconUrls {
    }
  }
  builderBaseLeague BuilderBaseLeague{
    name JsonLocalizedName{
    }
    id integer
  }
  role stringEnum:
    Array [ 5 ]
  warPreference stringEnum:
    Array [ 2 ]
  attackWins integer
  defenseWins integer
  townHallLevel integer
  townHallWeaponLevel integer
  legendStatistics PlayerLegendStatistics{
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
  troops PlayerItemLevelList[PlayerItemLevel{
    level integer
    name JsonLocalizedName{
    }
    maxLevel integer
    village stringEnum:
      [ HOME_VILLAGE, BUILDER_BASE, CLAN_CAPITAL ]
    superTroopIsActive boolean
    equipment {
    }
  }]
  heroes PlayerItemLevelList[PlayerItemLevel{
    level integer
    name JsonLocalizedName{
    }
    maxLevel integer
    village stringEnum:
      [ HOME_VILLAGE, BUILDER_BASE, CLAN_CAPITAL ]
    superTroopIsActive boolean
    equipment {
    }
  }]
  heroEquipment PlayerItemLevelList[PlayerItemLevel{
    level integer
    name JsonLocalizedName{
    }
    maxLevel integer
    village stringEnum:
      Array [ 3 ]
    superTroopIsActive boolean
    equipment {
    }
  }]
  spells PlayerItemLevelList[PlayerItemLevel{
    level integer
    name JsonLocalizedName{
    }
    maxLevel integer
    village stringEnum:
      Array [ 3 ]
    superTroopIsActive boolean
    equipment {
    }
  }]
  labels LabelList[Label{
    name JsonLocalizedName{
    }
    id integer
    iconUrls {
    }
  }]
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
  achievements PlayerAchievementProgressList[PlayerAchievementProgress{
    stars integer
    value integer
    name JsonLocalizedName{
    }
    target integer
    info JsonLocalizedName{
    }
    completionInfo JsonLocalizedName{
    }
    village stringEnum:
      [ HOME_VILLAGE, BUILDER_BASE, CLAN_CAPITAL ]
  }]
  clanCapitalContributions integer
  playerHouse PlayerHouse{
    elements PlayerHouseElementList[PlayerHouseElement{
      id integer
      type stringEnum:
        [ GROUND, ROOF, FOOT, DECO ]
    }]
  }
  currentLeagueGroupTag string
  currentLeagueSeasonId Long{
  }
  previousLeagueGroupTag string
  previousLeagueSeasonId Long{
  }
}
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

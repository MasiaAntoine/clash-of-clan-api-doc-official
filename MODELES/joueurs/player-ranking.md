# `PlayerRanking`

**Catégorie :** Joueurs

## Schéma

```
PlayerRanking{
  clan PlayerRankingClan{
    tag string
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
  attackWins integer
  defenseWins integer
  tag string
  name string
  expLevel integer
  rank integer
  previousRank integer
  trophies integer
}
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

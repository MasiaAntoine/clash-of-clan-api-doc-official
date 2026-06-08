# `PlayerBuilderBaseRanking`

**Catégorie :** Joueurs

## Schéma

```
PlayerBuilderBaseRanking{
  clan PlayerRankingClan{
    tag string
    name string
    badgeUrls {
    }
  }
  builderBaseLeague BuilderBaseLeague{
    name JsonLocalizedName{
    }
    id integer
  }
  tag string
  name string
  expLevel integer
  rank integer
  previousRank integer
  builderBaseTrophies integer
}
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

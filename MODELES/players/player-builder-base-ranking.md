# `PlayerBuilderBaseRanking`

**Category:** Players

## Schema

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

[← Models index](../README.md) · [← API documentation](../../README.md)

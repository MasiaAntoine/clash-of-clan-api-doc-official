# `PlayerRanking`

**Category:** Players

## Schema

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

[← Models index](../README.md) · [← API documentation](../../README.md)

# `PlayerAchievementProgress`

**Category:** Players

## Schema

```
PlayerAchievementProgress{
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
}
```

[← Models index](../README.md) · [← API documentation](../../README.md)

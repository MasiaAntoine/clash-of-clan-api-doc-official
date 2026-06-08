# `PlayerItemLevel`

**Category:** Players

## Schema

```
PlayerItemLevel{
  level integer
  name JsonLocalizedName{
  }
  maxLevel integer
  village stringEnum:
    Array [ 3 ]
  superTroopIsActive boolean
  equipment PlayerItemLevelList[{
  }]
}
```

[← Models index](../README.md) · [← API documentation](../../README.md)

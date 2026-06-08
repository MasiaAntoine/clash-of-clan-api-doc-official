# `ClanCapitalRaidSeasonDefenseLogEntry`

**Category:** Capital

## Schema

```
ClanCapitalRaidSeasonDefenseLogEntry{
  attacker ClanCapitalRaidSeasonClanInfo{
    tag string
    name string
    level integer
    badgeUrls {
    }
  }
  attackCount integer
  districtCount integer
  districtsDestroyed integer
  districts ClanCapitalRaidSeasonDistrictList[ClanCapitalRaidSeasonDistrict{
    stars integer
    name JsonLocalizedName{
    }
    id integer
    destructionPercent integer
    attackCount integer
    totalLooted integer
    attacks ClanCapitalRaidSeasonAttackList[ClanCapitalRaidSeasonAttack{
      attacker ClanCapitalRaidSeasonAttacker{
        tag string
        name string
      }
      destructionPercent integer
      stars integer
    }]
    districtHallLevel integer
  }]
}
```

[← Models index](../README.md) · [← API documentation](../../README.md)

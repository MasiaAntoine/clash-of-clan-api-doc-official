# `ClanMemberList[ClanMemberList`

**Category:** Clans

## Schema

```
ClanMemberList[ClanMemberList{
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
  tag string
  name string
  role stringEnum:
    [ NOT_MEMBER, MEMBER, LEADER, ADMIN, COLEADER ]
  townHallLevel integer
  expLevel integer
  clanRank integer
  previousClanRank integer
  donations integer
  donationsReceived integer
  trophies integer
  builderBaseTrophies integer
  playerHouse PlayerHouse{
    elements PlayerHouseElementList[PlayerHouseElement{
      id integer
      type stringEnum:
        [ GROUND, ROOF, FOOT, DECO ]
    }]
  }
}]
```

[← Models index](../README.md) · [← API documentation](../../README.md)

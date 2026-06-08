# `Clan`

**Category:** Clans

## Schema

```
Clan{
  memberList ClanMemberList[ClanMember{
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
  warLeague WarLeague{
    name JsonLocalizedName{
    }
    id integer
  }
  capitalLeague CapitalLeague{
    name JsonLocalizedName{
    }
    id integer
  }
  tag string
  clanBuilderBasePoints integer
  clanCapitalPoints integer
  requiredTrophies integer
  requiredBuilderBaseTrophies integer
  requiredTownhallLevel integer
  warFrequency stringEnum:
    [ UNKNOWN, ALWAYS, MORE_THAN_ONCE_PER_WEEK, ONCE_PER_WEEK, LESS_THAN_ONCE_PER_WEEK, NEVER, ANY ]
  clanLevel integer
  warWinStreak integer
  warWins integer
  warTies integer
  warLosses integer
  clanPoints integer
  isFamilyFriendly boolean
  isWarLogPublic boolean
  chatLanguage Language{
    name string
    id integer
    languageCode string
  }
  labels LabelList[Label{
    name JsonLocalizedName{
    }
    id integer
    iconUrls {
    }
  }]
  name string
  location Location{
    localizedName string
    id integer
    name string
    isCountry boolean
    countryCode string
  }
  type stringEnum:
    [ OPEN, INVITE_ONLY, CLOSED ]
  members integer
  description string
  clanCapital ClanCapital{
    capitalHallLevel integer
    districts ClanDistrictDataList[ClanDistrictData{
      name JsonLocalizedName{
      }
      id integer
      districtHallLevel integer
    }]
  }
  badgeUrls {
  }
}
```

[← Models index](../README.md) · [← API documentation](../../README.md)

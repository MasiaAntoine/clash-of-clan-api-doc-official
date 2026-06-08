# `ClanWarLogEntry`

**Category:** Wars

## Schema

```
ClanWarLogEntry{
  clan WarClan{
    destructionPercentage Float{
    }
    tag string
    name string
    badgeUrls {
    }
    clanLevel integer
    attacks integer
    stars integer
    expEarned integer
    members ClanWarMemberList[ClanWarMember{
      tag string
      name string
      mapPosition integer
      townhallLevel integer
      opponentAttacks integer
      bestOpponentAttack ClanWarAttack{
        order integer
        attackerTag string
        defenderTag string
        stars integer
        destructionPercentage integer
        duration integer
      }
      attacks ClanWarAttackList[ClanWarAttack{
        order integer
        attackerTag string
        defenderTag string
        stars integer
        destructionPercentage integer
        duration integer
      }]
    }]
  }
  teamSize integer
  attacksPerMember integer
  battleModifier stringEnum:
    [ NONE, HARD_MODE ]
  opponent WarClan{
    destructionPercentage Float{
    }
    tag string
    name string
    badgeUrls {
    }
    clanLevel integer
    attacks integer
    stars integer
    expEarned integer
    members ClanWarMemberList[ClanWarMember{
      tag string
      name string
      mapPosition integer
      townhallLevel integer
      opponentAttacks integer
      bestOpponentAttack ClanWarAttack{
        order integer
        attackerTag string
        defenderTag string
        stars integer
        destructionPercentage integer
        duration integer
      }
      attacks ClanWarAttackList[ClanWarAttack{
        order integer
        attackerTag string
        defenderTag string
        stars integer
        destructionPercentage integer
        duration integer
      }]
    }]
  }
  endTime string
  result stringEnum:
    [ LOSE, WIN, TIE ]
}
```

[← Models index](../README.md) · [← API documentation](../../README.md)

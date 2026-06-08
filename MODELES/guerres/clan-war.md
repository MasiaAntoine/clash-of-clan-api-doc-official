# `ClanWar`

**Catégorie :** Guerres

## Schéma

```
ClanWar{
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
  startTime string
  state stringEnum:
    [ CLAN_NOT_FOUND, ACCESS_DENIED, NOT_IN_WAR, IN_MATCHMAKING, ENTER_WAR, MATCHED, PREPARATION, WAR, IN_WAR, ENDED ]
  endTime string
  preparationStartTime string
}
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

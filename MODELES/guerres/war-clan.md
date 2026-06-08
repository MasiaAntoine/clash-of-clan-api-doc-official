# `WarClan`

**Catégorie :** Guerres

## Schéma

```
WarClan{
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
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

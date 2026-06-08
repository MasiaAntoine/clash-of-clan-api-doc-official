# `ClanWarMember`

**Catégorie :** Guerres

## Schéma

```
ClanWarMember{
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
}
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

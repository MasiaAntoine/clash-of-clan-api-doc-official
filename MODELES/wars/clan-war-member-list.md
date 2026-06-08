# `ClanWarMemberList[ClanWarMemberList`

**Category:** Wars

## Schema

```
ClanWarMemberList[ClanWarMemberList{
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
```

[← Models index](../README.md) · [← API documentation](../../README.md)

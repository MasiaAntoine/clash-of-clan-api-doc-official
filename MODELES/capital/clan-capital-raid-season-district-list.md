# `ClanCapitalRaidSeasonDistrictList[ClanCapitalRaidSeasonDistrictList`

**Catégorie :** Capitale

## Schéma

```
ClanCapitalRaidSeasonDistrictList[ClanCapitalRaidSeasonDistrictList{
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
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

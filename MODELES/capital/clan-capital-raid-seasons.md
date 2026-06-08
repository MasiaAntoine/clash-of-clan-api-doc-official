# `ClanCapitalRaidSeasons[ClanCapitalRaidSeasons`

**Catégorie :** Capitale

## Schéma

```
ClanCapitalRaidSeasons[ClanCapitalRaidSeasons{
  attackLog ClanCapitalRaidSeasonAttackLogList[ClanCapitalRaidSeasonAttackLogEntry{
    defender ClanCapitalRaidSeasonClanInfo{
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
  }]
  defenseLog ClanCapitalRaidSeasonDefenseLogList[ClanCapitalRaidSeasonDefenseLogEntry{
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
  }]
  state string
  startTime string
  endTime string
  capitalTotalLoot integer
  raidsCompleted integer
  totalAttacks integer
  enemyDistrictsDestroyed integer
  offensiveReward integer
  defensiveReward integer
  members ClanCapitalRaidSeasonMemberList[ClanCapitalRaidSeasonMember{
    tag string
    name string
    attacks integer
    attackLimit integer
    bonusAttackLimit integer
    capitalResourcesLooted integer
  }]
}]
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

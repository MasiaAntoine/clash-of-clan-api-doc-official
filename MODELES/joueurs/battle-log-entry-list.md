# `BattleLogEntryList[BattleLogEntryList`

**Catégorie :** Joueurs

## Schéma

```
BattleLogEntryList[BattleLogEntryList{
  battleType stringEnum:
    [ HOME_VILLAGE, RANKED, LEGEND ]
  attack boolean
  armyShareCode string
  opponentPlayerTag string
  stars integer
  destructionPercentage integer
  lootedResources BattleLogResourceList[Resource{
    name string
    amount long{
    }
  }]
  extraLootedResources BattleLogResourceList[Resource{
    name string
    amount long{
    }
  }]
  availableLoot BattleLogResourceList[Resource{
    name string
    amount long{
    }
  }]
}]
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

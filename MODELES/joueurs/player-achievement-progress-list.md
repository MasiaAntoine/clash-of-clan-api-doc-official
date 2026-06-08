# `PlayerAchievementProgressList[PlayerAchievementProgressList`

**Catégorie :** Joueurs

## Schéma

```
PlayerAchievementProgressList[PlayerAchievementProgressList{
  stars integer
  value integer
  name JsonLocalizedName{
  }
  target integer
  info JsonLocalizedName{
  }
  completionInfo JsonLocalizedName{
  }
  village stringEnum:
    [ HOME_VILLAGE, BUILDER_BASE, CLAN_CAPITAL ]
}]
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

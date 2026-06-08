# `PlayerItemLevel`

**Catégorie :** Joueurs

## Schéma

```
PlayerItemLevel{
  level integer
  name JsonLocalizedName{
  }
  maxLevel integer
  village stringEnum:
    Array [ 3 ]
  superTroopIsActive boolean
  equipment PlayerItemLevelList[{
  }]
}
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

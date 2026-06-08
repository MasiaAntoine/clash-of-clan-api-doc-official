# `PlayerHouse`

**Catégorie :** Joueurs

## Schéma

```
PlayerHouse{
  elements PlayerHouseElementList[PlayerHouseElement{
    id integer
    type stringEnum:
      [ GROUND, ROOF, FOOT, DECO ]
  }]
}
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

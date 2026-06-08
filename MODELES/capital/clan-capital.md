# `ClanCapital`

**Catégorie :** Capitale

## Schéma

```
ClanCapital{
  capitalHallLevel integer
  districts ClanDistrictDataList[ClanDistrictData{
    name JsonLocalizedName{
    }
    id integer
    districtHallLevel integer
  }]
}
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

# `ClanRankingList[ClanRankingList`

**Catégorie :** Localisations

## Schéma

```
ClanRankingList[ClanRankingList{
  clanLevel integer
  clanPoints integer
  location Location{
    localizedName string
    id integer
    name string
    isCountry boolean
    countryCode string
  }
  members integer
  tag string
  name string
  rank integer
  previousRank integer
  badgeUrls {
  }
}]
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

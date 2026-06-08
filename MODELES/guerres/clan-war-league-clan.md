# `ClanWarLeagueClan`

**Catégorie :** Guerres

## Schéma

```
ClanWarLeagueClan{
  tag string
  clanLevel integer
  name string
  members ClanWarLeagueClanMemberList[ClanWarLeagueClanMember{
    tag string
    townHallLevel integer
    name string
  }]
  badgeUrls {
  }
}
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

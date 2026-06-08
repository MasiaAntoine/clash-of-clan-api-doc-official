# `WarStatusList[WarStatusList`

**Catégorie :** Guerres

## Schéma

```
WarStatusList[WarStatusList{
  statusCode integer
  clanTag string
  enemyClanTag string
  warState stringEnum:
    [ CLAN_NOT_FOUND, ACCESS_DENIED, NOT_IN_WAR, IN_MATCHMAKING, ENTER_WAR, MATCHED, PREPARATION, WAR, IN_WAR, ENDED ]
  timestamp string
}]
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

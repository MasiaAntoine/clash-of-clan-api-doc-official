# `LeagueGroup`

**Catégorie :** Ligues

## Schéma

```
LeagueGroup{
  members LeagueGroupMemberList[LeagueGroupMember{
    playerTag string
    playerName string
    clanTag string
    clanName string
    leagueTrophies integer
    attackWinCount integer
    attackLoseCount integer
    defenseWinCount integer
    defenseLoseCount integer
  }]
  attackLogs LeagueGroupBattleLogEntryList[LeagueBattleLogEntry{
    opponentPlayerTag string
    opponentName string
    stars integer
    destructionPercentage integer
    trophies integer
    creationTime string
  }]
  defenseLogs LeagueGroupBattleLogEntryList[LeagueBattleLogEntry{
    opponentPlayerTag string
    opponentName string
    stars integer
    destructionPercentage integer
    trophies integer
    creationTime string
  }]
}
```

[← Index des modèles](../README.md) · [← Documentation API](../../README.md)

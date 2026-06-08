# `LeagueGroup`

**Category:** Leagues

## Schema

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

[← Models index](../README.md) · [← API documentation](../../README.md)

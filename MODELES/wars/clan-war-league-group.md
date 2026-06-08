# `ClanWarLeagueGroup`

**Category:** Wars

## Schema

```
ClanWarLeagueGroup{
  tag string
  state stringEnum:
    [ GROUP_NOT_FOUND, NOT_IN_WAR, PREPARATION, WAR, ENDED ]
  season string
  clans ClanWarLeagueClanList[ClanWarLeagueClan{
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
  }]
  rounds ClanWarLeagueRoundList[ClanWarLeagueRound{
    warTags StringList[string]
  }]
}
```

[← Models index](../README.md) · [← API documentation](../../README.md)

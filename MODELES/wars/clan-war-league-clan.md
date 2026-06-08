# `ClanWarLeagueClan`

**Category:** Wars

## Schema

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

[← Models index](../README.md) · [← API documentation](../../README.md)

# `ClanRanking`

**Category:** Locations

## Schema

```
ClanRanking{
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
}
```

[← Models index](../README.md) · [← API documentation](../../README.md)

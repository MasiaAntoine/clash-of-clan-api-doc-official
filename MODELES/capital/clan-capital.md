# `ClanCapital`

**Category:** Capital

## Schema

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

[← Models index](../README.md) · [← API documentation](../../README.md)

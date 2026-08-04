
# Devices Request Filter

## Class Name

`DevicesRequestFilter`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`DevicesFilter`](../../../doc/models/devices-filter.md) | DevicesRequestFilter.fromDevicesFilter(DevicesFilter devicesFilter) |
| [`PaginationFilter`](../../../doc/models/pagination-filter.md) | DevicesRequestFilter.fromPaginationFilter(PaginationFilter paginationFilter) |

## DevicesFilter

### Initialization Code

#### Example

```java
DevicesRequestFilter.fromDevicesFilter(
        new DevicesFilter.Builder()
            .mecId("tsp-testmec-1-eks-dev-edge-us-east-1-imp-dev")
            .build()
    )
```

## PaginationFilter

### Initialization Code

#### Example

```java
DevicesRequestFilter.fromPaginationFilter(
        new PaginationFilter.Builder(
            "H4sICCP5CWkA_25leHQAjM_BCoMwDAbgd_npsUKceOlz7LRbq1UCtbqaDob47mNlgw0GE_7Tn4-QbFCBJ5aYJ-cTTEukX5Ud5NmAiOqq5ExkSi74Qhy7kFe--X_a-WFOB9WRpYsd_fvyWkPJLDZ0c44C09CpaRsNdc0-3T8nkrLXUAOH8uAGxyFwHG1XAPcw4GmpxK_Ccayc5R67_sWwPwIAAP__njV5tUEBAAA="
        )
        .build()
    )
```


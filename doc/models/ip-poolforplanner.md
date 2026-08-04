
# IP Poolforplanner

## Structure

`IPPoolforplanner`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IsDefaultPool` | `Boolean` | Optional | - | Boolean getIsDefaultPool() | setIsDefaultPool(Boolean isDefaultPool) |
| `PoolName` | `String` | Optional | - | String getPoolName() | setPoolName(String poolName) |
| `PoolType` | `String` | Optional | - | String getPoolType() | setPoolType(String poolType) |

## Example

```java
import com.verizon.thingspace.models.IPPoolforplanner;

IPPoolforplanner iPPoolforplanner = new IPPoolforplanner.Builder()
    .isDefaultPool(false)
    .poolName("poolName2")
    .poolType("poolType4")
    .build();
```


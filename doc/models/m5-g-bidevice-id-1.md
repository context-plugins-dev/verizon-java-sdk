
# M5 G Bidevice Id 1

## Structure

`M5gBideviceId1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `Kind` | `String` | Optional | - | String getKind() | setKind(String kind) |

## Example

```java
import com.verizon.thingspace.models.M5gBideviceId1;

M5gBideviceId1 m5gBideviceId1 = new M5gBideviceId1.Builder()
    .id("15-digit IMSI")
    .kind("imsi")
    .build();
```


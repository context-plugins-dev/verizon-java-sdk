
# Device Id 2

## Structure

`DeviceId2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `Kind` | `String` | Optional | - | String getKind() | setKind(String kind) |

## Example

```java
import com.verizon.thingspace.models.DeviceId2;

DeviceId2 deviceId2 = new DeviceId2.Builder()
    .id("15-digit IMEI")
    .kind("imei")
    .build();
```


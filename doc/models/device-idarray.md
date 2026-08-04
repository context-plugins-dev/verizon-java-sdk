
# Device Idarray

## Structure

`DeviceIdarray`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Kind` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9]{3,32}$` | String getKind() | setKind(String kind) |
| `Id` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Za-z0-9]{3,32}$` | String getId() | setId(String id) |

## Example

```java
import com.verizon.thingspace.models.DeviceIdarray;

DeviceIdarray deviceIdarray = new DeviceIdarray.Builder()
    .kind("imei")
    .id("id8")
    .build();
```


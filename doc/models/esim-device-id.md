
# ESIM Device Id

## Structure

`ESIMDeviceId`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `Kind` | `String` | Optional | - | String getKind() | setKind(String kind) |

## Example

```java
import com.verizon.thingspace.models.ESIMDeviceId;

ESIMDeviceId eSIMDeviceId = new ESIMDeviceId.Builder()
    .id("32-digit EID")
    .kind("eid")
    .build();
```


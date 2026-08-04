
# Ready Sim Device Id

## Structure

`ReadySimDeviceId`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Kind` | `String` | Optional | - | String getKind() | setKind(String kind) |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |

## Example

```java
import com.verizon.thingspace.models.ReadySimDeviceId;

ReadySimDeviceId readySimDeviceId = new ReadySimDeviceId.Builder()
    .kind("iccid")
    .id("20-digit iccid")
    .build();
```


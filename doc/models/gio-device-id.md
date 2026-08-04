
# GIO Device Id

## Structure

`GIODeviceId`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Kind` | `String` | Required | - | String getKind() | setKind(String kind) |
| `Id` | `String` | Required | - | String getId() | setId(String id) |

## Example

```java
import com.verizon.thingspace.models.GIODeviceId;

GIODeviceId gIODeviceId = new GIODeviceId.Builder(
    "eid",
    "12345678901234567890123456789012"
)
.build();
```


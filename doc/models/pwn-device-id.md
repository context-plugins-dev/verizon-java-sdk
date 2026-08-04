
# PWN Device Id

## Structure

`PWNDeviceId`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | - | String getId() | setId(String id) |
| `Kind` | `String` | Required | - | String getKind() | setKind(String kind) |

## Example

```java
import com.verizon.thingspace.models.PWNDeviceId;

PWNDeviceId pWNDeviceId = new PWNDeviceId.Builder(
    "99948099913024600001",
    "iccid"
)
.build();
```


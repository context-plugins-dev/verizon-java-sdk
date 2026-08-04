
# Qos Device Id

## Structure

`QosDeviceId`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `Kind` | `String` | Optional | - | String getKind() | setKind(String kind) |

## Example

```java
import com.verizon.thingspace.models.QosDeviceId;

QosDeviceId qosDeviceId = new QosDeviceId.Builder()
    .id("10-digit phone number")
    .kind("mdn")
    .build();
```


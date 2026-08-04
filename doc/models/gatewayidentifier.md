
# Gatewayidentifier

## Structure

`Gatewayidentifier`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Deviceid` | `String` | Optional | a unique parent deviceid used to group all Lora sensors. Sensors need parent gateway for connection | String getDeviceid() | setDeviceid(String deviceid) |

## Example

```java
import com.verizon.thingspace.models.Gatewayidentifier;

Gatewayidentifier gatewayidentifier = new Gatewayidentifier.Builder()
    .deviceid("UUID of the Gateway device")
    .build();
```


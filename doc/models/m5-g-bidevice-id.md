
# M5 G Bidevice Id

## Structure

`M5gBideviceId`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | [`M5gBideviceId1`](../../doc/models/m5-g-bidevice-id-1.md) | Optional | - | M5gBideviceId1 getDeviceId() | setDeviceId(M5gBideviceId1 deviceId) |

## Example

```java
import com.verizon.thingspace.models.M5gBideviceId;
import com.verizon.thingspace.models.M5gBideviceId1;

M5gBideviceId m5gBideviceId = new M5gBideviceId.Builder()
    .deviceId(new M5gBideviceId1.Builder()
        .id("id0")
        .kind("kind8")
        .build())
    .build();
```


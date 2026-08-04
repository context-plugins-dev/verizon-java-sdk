
# M5 G Bidevice Idarray 2

## Structure

`M5gBideviceIdarray2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | [`List<M5gBideviceId1>`](../../doc/models/m5-g-bidevice-id-1.md) | Optional | - | List<M5gBideviceId1> getDeviceId() | setDeviceId(List<M5gBideviceId1> deviceId) |

## Example

```java
import com.verizon.thingspace.models.M5gBideviceId1;
import com.verizon.thingspace.models.M5gBideviceIdarray2;
import java.util.Arrays;

M5gBideviceIdarray2 m5gBideviceIdarray2 = new M5gBideviceIdarray2.Builder()
    .deviceId(Arrays.asList(
        new M5gBideviceId1.Builder()
            .id("id0")
            .kind("kind8")
            .build()
    ))
    .build();
```


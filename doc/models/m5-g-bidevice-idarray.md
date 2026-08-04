
# M5 G Bidevice Idarray

## Structure

`M5gBideviceIdarray`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | [`List<M5gBideviceIdarrayDeviceId>`](../../doc/models/containers/m5-g-bidevice-idarray-device-id.md) | Optional | This is List of a container for any-of cases. | List<M5gBideviceIdarrayDeviceId> getDeviceId() | setDeviceId(List<M5gBideviceIdarrayDeviceId> deviceId) |

## Example

```java
import com.verizon.thingspace.models.M5gBideviceId1;
import com.verizon.thingspace.models.M5gBideviceIdarray;
import com.verizon.thingspace.models.containers.M5gBideviceIdarrayDeviceId;
import java.util.Arrays;

M5gBideviceIdarray m5gBideviceIdarray = new M5gBideviceIdarray.Builder()
    .deviceId(Arrays.asList(
        M5gBideviceIdarrayDeviceId.fromM5gBideviceId1(
            new M5gBideviceId1.Builder()
                .id("id0")
                .kind("kind8")
                .build()
        ),
        M5gBideviceIdarrayDeviceId.fromM5gBideviceId1(
            new M5gBideviceId1.Builder()
                .id("id0")
                .kind("kind8")
                .build()
        ),
        M5gBideviceIdarrayDeviceId.fromM5gBideviceId1(
            new M5gBideviceId1.Builder()
                .id("id0")
                .kind("kind8")
                .build()
        )
    ))
    .build();
```


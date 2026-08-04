
# Device List with Service Address 1

## Structure

`DeviceListWithServiceAddress1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | [`List<DeviceListWithServiceAddress1DeviceId>`](../../doc/models/containers/device-list-with-service-address-1-device-id.md) | Optional | This is List of a container for any-of cases. | List<DeviceListWithServiceAddress1DeviceId> getDeviceId() | setDeviceId(List<DeviceListWithServiceAddress1DeviceId> deviceId) |
| `PrimaryPlaceofuse` | [`M5gBiprimaryPlaceofuse`](../../doc/models/m5-g-biprimary-placeofuse.md) | Optional | - | M5gBiprimaryPlaceofuse getPrimaryPlaceofuse() | setPrimaryPlaceofuse(M5gBiprimaryPlaceofuse primaryPlaceofuse) |

## Example

```java
import com.verizon.thingspace.models.DeviceListWithServiceAddress1;
import com.verizon.thingspace.models.M5gBiAddress;
import com.verizon.thingspace.models.M5gBiCustomerName;
import com.verizon.thingspace.models.M5gBideviceId1;
import com.verizon.thingspace.models.M5gBiprimaryPlaceofuse;
import com.verizon.thingspace.models.containers.DeviceListWithServiceAddress1DeviceId;
import java.util.Arrays;

DeviceListWithServiceAddress1 deviceListWithServiceAddress1 = new DeviceListWithServiceAddress1.Builder()
    .deviceId(Arrays.asList(
        DeviceListWithServiceAddress1DeviceId.fromM5gBideviceId1(
            new M5gBideviceId1.Builder()
                .id("id0")
                .kind("kind8")
                .build()
        ),
        DeviceListWithServiceAddress1DeviceId.fromM5gBideviceId1(
            new M5gBideviceId1.Builder()
                .id("id0")
                .kind("kind8")
                .build()
        )
    ))
    .primaryPlaceofuse(new M5gBiprimaryPlaceofuse.Builder()
        .address(new M5gBiAddress.Builder()
            .addressLine1("addressLine18")
            .city("city6")
            .state("state2")
            .zip("zip0")
            .zip4("zip+48")
            .build())
        .customerName(new M5gBiCustomerName.Builder()
            .firstName("firstName4")
            .lastName("lastName4")
            .middleName("middleName8")
            .title("title4")
            .suffex("suffex4")
            .build())
        .build())
    .build();
```


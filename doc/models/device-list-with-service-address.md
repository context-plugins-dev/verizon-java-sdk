
# Device List with Service Address

## Structure

`DeviceListWithServiceAddress`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | [`List<M5gBideviceId1>`](../../doc/models/m5-g-bidevice-id-1.md) | Optional | - | List<M5gBideviceId1> getDeviceId() | setDeviceId(List<M5gBideviceId1> deviceId) |
| `PrimaryPlaceofuse` | [`M5gBiaddressAndcustomerinfo`](../../doc/models/m5-g-biaddress-andcustomerinfo.md) | Optional | - | M5gBiaddressAndcustomerinfo getPrimaryPlaceofuse() | setPrimaryPlaceofuse(M5gBiaddressAndcustomerinfo primaryPlaceofuse) |

## Example

```java
import com.verizon.thingspace.models.DeviceListWithServiceAddress;
import com.verizon.thingspace.models.M5gBiAddress;
import com.verizon.thingspace.models.M5gBiCustomerName;
import com.verizon.thingspace.models.M5gBiaddressAndcustomerinfo;
import com.verizon.thingspace.models.M5gBideviceId1;
import com.verizon.thingspace.models.M5gBiprimaryPlaceofuse;
import java.util.Arrays;

DeviceListWithServiceAddress deviceListWithServiceAddress = new DeviceListWithServiceAddress.Builder()
    .deviceId(Arrays.asList(
        new M5gBideviceId1.Builder()
            .id("id0")
            .kind("kind8")
            .build()
    ))
    .primaryPlaceofuse(new M5gBiaddressAndcustomerinfo.Builder()
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
        .build())
    .build();
```


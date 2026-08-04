
# Get Device Statuses Requestforplanner

## Structure

`GetDeviceStatusesRequestforplanner`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountNumber` | `String` | Optional | The numeric name of the account, including leading zeros. | String getAccountNumber() | setAccountNumber(String accountNumber) |
| `RequestId` | `String` | Optional | The unique ID of a request. This is a UUID value. | String getRequestId() | setRequestId(String requestId) |
| `Devices` | [`List<DeviceListforplanner>`](../../doc/models/device-listforplanner.md) | Optional | - | List<DeviceListforplanner> getDevices() | setDevices(List<DeviceListforplanner> devices) |

## Example

```java
import com.verizon.thingspace.models.DeviceIdforplanner;
import com.verizon.thingspace.models.DeviceListforplanner;
import com.verizon.thingspace.models.GetDeviceStatusesRequestforplanner;
import com.verizon.thingspace.models.PrivateNetworkApns;
import java.util.Arrays;

GetDeviceStatusesRequestforplanner getDeviceStatusesRequestforplanner = new GetDeviceStatusesRequestforplanner.Builder()
    .accountNumber("0000123456-00001")
    .requestId("d24cc6e4-eeee-ffff-gggg-0ffbb091c076")
    .devices(Arrays.asList(
        new DeviceListforplanner.Builder()
            .deviceIds(Arrays.asList(
                new DeviceIdforplanner.Builder()
                    .kind("kind8")
                    .id("id0")
                    .build()
            ))
            .privateNetworkApns(Arrays.asList(
                new PrivateNetworkApns.Builder()
                    .apnName("apnName2")
                    .addressAssignmentMethod("addressAssignmentMethod8")
                    .ipaddress("ipAddress4")
                    .build(),
                new PrivateNetworkApns.Builder()
                    .apnName("apnName2")
                    .addressAssignmentMethod("addressAssignmentMethod8")
                    .ipaddress("ipAddress4")
                    .build()
            ))
            .ipaddress("ipAddress4")
            .activationCode("activationCode2")
            .build()
    ))
    .build();
```


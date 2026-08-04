
# Get Device Statuses Responseforplanner

## Structure

`GetDeviceStatusesResponseforplanner`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountNumber` | `String` | Optional | The numeric name of the account, including leading zeros. | String getAccountNumber() | setAccountNumber(String accountNumber) |
| `RequestId` | `String` | Optional | - | String getRequestId() | setRequestId(String requestId) |
| `DeviceStatusList` | [`List<DeviceStatusItemforplanner>`](../../doc/models/device-status-itemforplanner.md) | Optional | - | List<DeviceStatusItemforplanner> getDeviceStatusList() | setDeviceStatusList(List<DeviceStatusItemforplanner> deviceStatusList) |

## Example

```java
import com.verizon.thingspace.models.DeviceIdforplanner;
import com.verizon.thingspace.models.DeviceStatusItemforplanner;
import com.verizon.thingspace.models.GetDeviceStatusesResponseforplanner;
import java.util.Arrays;

GetDeviceStatusesResponseforplanner getDeviceStatusesResponseforplanner = new GetDeviceStatusesResponseforplanner.Builder()
    .accountNumber("0000123456-00001")
    .requestId("requestId4")
    .deviceStatusList(Arrays.asList(
        new DeviceStatusItemforplanner.Builder()
            .deviceIds(Arrays.asList(
                new DeviceIdforplanner.Builder()
                    .kind("kind8")
                    .id("id0")
                    .build()
            ))
            .status("status6")
            .reason("reason2")
            .build(),
        new DeviceStatusItemforplanner.Builder()
            .deviceIds(Arrays.asList(
                new DeviceIdforplanner.Builder()
                    .kind("kind8")
                    .id("id0")
                    .build()
            ))
            .status("status6")
            .reason("reason2")
            .build(),
        new DeviceStatusItemforplanner.Builder()
            .deviceIds(Arrays.asList(
                new DeviceIdforplanner.Builder()
                    .kind("kind8")
                    .id("id0")
                    .build()
            ))
            .status("status6")
            .reason("reason2")
            .build()
    ))
    .build();
```


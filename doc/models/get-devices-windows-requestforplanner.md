
# Get Devices Windows Requestforplanner

## Structure

`GetDevicesWindowsRequestforplanner`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountNumber` | `String` | Optional | The numeric name of the account, including leading zeros. | String getAccountNumber() | setAccountNumber(String accountNumber) |
| `Filter` | `String` | Optional | what windows to filter for: All - all 24 windows in a day, Best - top 3 windows by RAN KPI, Worst - lowest 3 windows by RAN KPI | String getFilter() | setFilter(String filter) |
| `Devices` | [`List<DeviceListforplanner>`](../../doc/models/device-listforplanner.md) | Optional | - | List<DeviceListforplanner> getDevices() | setDevices(List<DeviceListforplanner> devices) |

## Example

```java
import com.verizon.thingspace.models.DeviceIdforplanner;
import com.verizon.thingspace.models.DeviceListforplanner;
import com.verizon.thingspace.models.GetDevicesWindowsRequestforplanner;
import com.verizon.thingspace.models.PrivateNetworkApns;
import java.util.Arrays;

GetDevicesWindowsRequestforplanner getDevicesWindowsRequestforplanner = new GetDevicesWindowsRequestforplanner.Builder()
    .accountNumber("0000123456-00001")
    .filter("filter8")
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
            .build(),
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
            .build(),
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


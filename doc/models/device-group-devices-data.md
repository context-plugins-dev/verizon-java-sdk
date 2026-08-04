
# Device Group Devices Data

Returns the name, description, and list of devices in a device group.

## Structure

`DeviceGroupDevicesData`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | The description of the device group. | String getDescription() | setDescription(String description) |
| `Devices` | [`List<AccountDeviceList>`](../../doc/models/account-device-list.md) | Optional | The devices in the device group. | List<AccountDeviceList> getDevices() | setDevices(List<AccountDeviceList> devices) |
| `HasMoreData` | `Boolean` | Optional | False for a status 200 response.True for a status 202 response, indicating that there is more data to be retrieved. | Boolean getHasMoreData() | setHasMoreData(Boolean hasMoreData) |
| `Name` | `String` | Optional | The name of the device group. | String getName() | setName(String name) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceList;
import com.verizon.thingspace.models.DeviceGroupDevicesData;
import com.verizon.thingspace.models.DeviceId;
import java.util.Arrays;

DeviceGroupDevicesData deviceGroupDevicesData = new DeviceGroupDevicesData.Builder()
    .description("All service trucks in Nebraska.")
    .devices(Arrays.asList(
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "12345",
                    "meid"
                )
                .build(),
                new DeviceId.Builder(
                    "54321",
                    "mdn"
                )
                .build()
            )
        )
        .ipaddress("ipAddress4")
        .build()
    ))
    .hasMoreData(false)
    .name("Nebraska Trucks")
    .build();
```


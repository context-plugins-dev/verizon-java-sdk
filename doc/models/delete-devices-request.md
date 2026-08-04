
# Delete Devices Request

Request to delete a device request.

## Structure

`DeleteDevicesRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DevicesToDelete` | [`List<AccountDeviceList>`](../../doc/models/account-device-list.md) | Required | A list of up to 100 devices that you want to delete, specified by device identifier. You only need to provide one identifier per device. | List<AccountDeviceList> getDevicesToDelete() | setDevicesToDelete(List<AccountDeviceList> devicesToDelete) |
| `AccountName` | `String` | Optional | The Verizon billing account that the device group belongs to. An account name is usually numeric, and must include any leading zeros. | String getAccountName() | setAccountName(String accountName) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceList;
import com.verizon.thingspace.models.DeleteDevicesRequest;
import com.verizon.thingspace.models.DeviceId;
import java.util.Arrays;

DeleteDevicesRequest deleteDevicesRequest = new DeleteDevicesRequest.Builder(
    Arrays.asList(
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "09005470263",
                    "esn"
                )
                .build()
            )
        )
        .ipaddress("ipAddress8")
        .build(),
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "85000022411113460014",
                    "iccid"
                )
                .build()
            )
        )
        .ipaddress("ipAddress8")
        .build(),
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "85000022412313460016",
                    "iccid"
                )
                .build()
            )
        )
        .ipaddress("ipAddress8")
        .build()
    )
)
.accountName("accountName0")
.build();
```


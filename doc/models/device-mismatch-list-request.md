
# Device Mismatch List Request

Request to list of all 4G devices with an ICCID (SIM) that was not activated with the expected IMEI (hardware) during a specified time frame.

## Structure

`DeviceMismatchListRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Filter` | [`DateFilter`](../../doc/models/date-filter.md) | Required | Filter out the dates. | DateFilter getFilter() | setFilter(DateFilter filter) |
| `Devices` | [`List<AccountDeviceList>`](../../doc/models/account-device-list.md) | Optional | A list of specific devices that you want to check, specified by ICCID or MDN. | List<AccountDeviceList> getDevices() | setDevices(List<AccountDeviceList> devices) |
| `AccountName` | `String` | Optional | The account that you want to search for mismatched devices. If you don't specify an accountName, the search includes all devices to which you have access. | String getAccountName() | setAccountName(String accountName) |
| `GroupName` | `String` | Optional | The name of a device group, to only include devices in that group. | String getGroupName() | setGroupName(String groupName) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceList;
import com.verizon.thingspace.models.DateFilter;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceMismatchListRequest;
import java.util.Arrays;

DeviceMismatchListRequest deviceMismatchListRequest = new DeviceMismatchListRequest.Builder(
    new DateFilter.Builder(
        "2020-05-01T15:00:00-08:00Z",
        "2020-07-30T15:00:00-08:00Z"
    )
    .build()
)
.devices(Arrays.asList(
        new AccountDeviceList.Builder(
            Arrays.asList(
                new DeviceId.Builder(
                    "8914800000080078",
                    "ICCID"
                )
                .build(),
                new DeviceId.Builder(
                    "5096300587",
                    "MDN"
                )
                .build()
            )
        )
        .ipaddress("ipAddress4")
        .build()
    ))
.accountName("0342077109-00001")
.groupName("groupName4")
.build();
```


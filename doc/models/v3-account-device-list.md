
# V3 Account Device List

Array of devices.

## Structure

`V3AccountDeviceList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account name. | String getAccountName() | setAccountName(String accountName) |
| `HasMoreData` | `boolean` | Required | Has more device flag? | boolean getHasMoreData() | setHasMoreData(boolean hasMoreData) |
| `LastSeenDeviceId` | `String` | Optional | Last seen device identifier. | String getLastSeenDeviceId() | setLastSeenDeviceId(String lastSeenDeviceId) |
| `MaxPageSize` | `int` | Required | Maximum page size. | int getMaxPageSize() | setMaxPageSize(int maxPageSize) |
| `DeviceList` | [`List<V3AccountDevice>`](../../doc/models/v3-account-device.md) | Required | Account device list. | List<V3AccountDevice> getDeviceList() | setDeviceList(List<V3AccountDevice> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V3AccountDevice;
import com.verizon.thingspace.models.V3AccountDeviceList;
import com.verizon.thingspace.models.V3SoftwareInfo;
import java.util.Arrays;

V3AccountDeviceList v3AccountDeviceList = new V3AccountDeviceList.Builder(
    "0000123456-00001",
    true,
    1000,
    Arrays.asList(
        new V3AccountDevice.Builder(
            "15-digit device ID",
            "10-digit MDN",
            "BG96",
            "QUECTEL",
            "BG96MAR04A04M1G",
            false,
            "Active",
            true,
            "LWM2M",
            Arrays.asList(
                new V3SoftwareInfo.Builder(
                    "VZ_MDM_IOT",
                    "0.14",
                    "2012-04-23T18:25:43.511Z"
                )
                .build()
            )
        )
        .fileList(Arrays.asList(
                new V3SoftwareInfo.Builder(
                    "VZ_MDM_IOT",
                    "0.14",
                    "2012-04-23T18:25:43.511Z"
                )
                .build()
            ))
        .createTime("2021-06-03 00:03:56.079 +0000 UTC")
        .upgradeTime("2021-06-03 00:03:56.079 +0000 UTC")
        .updateTime("2021-06-03 00:03:56.079 +0000 UTC")
        .refreshTime("2021-06-03 00:03:56.079 +0000 UTC")
        .build()
    )
)
.lastSeenDeviceId("15-digit IMEI")
.build();
```



# Device List Result

Device list information.

## Structure

`DeviceListResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account name. | String getAccountName() | setAccountName(String accountName) |
| `DeviceCount` | `int` | Required | Total device count. | int getDeviceCount() | setDeviceCount(int deviceCount) |
| `DeviceList` | [`List<V3Device>`](../../doc/models/v3-device.md) | Required | List of devices with id in IMEI.<br><br>**Constraints**: *Maximum Items*: `1000` | List<V3Device> getDeviceList() | setDeviceList(List<V3Device> deviceList) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DeviceListResult;
import com.verizon.thingspace.models.V3Device;
import java.util.Arrays;

DeviceListResult deviceListResult = new DeviceListResult.Builder(
    "0000123456-00001",
    1,
    Arrays.asList(
        new V3Device.Builder(
            "15-digit IMEI"
        )
        .requestStatus("requestStatus2")
        .resultReason("resultReason2")
        .mdn("10-digit MDN")
        .model("GM01Q")
        .make("SEQUANS COMMUNICATIONS")
        .firmware("SR1.2.0.0-10657")
        .fotaEligible(true)
        .status("Active")
        .licenseAssigned(true)
        .protocol("LWM2M")
        .createTime("2021-06-03 00:03:56.079 +0000 UTC")
        .statusTime("2021-06-03 00:03:56.079 +0000 UTC")
        .refreshTime("2021-06-03 00:03:56.079 +0000 UTC")
        .lastConnectionTime(DateTimeHelper.fromRfc8601DateTime("2012-04-23T18:25:43.511Z"))
        .build()
    )
)
.build();
```



# V2 Account Device List

List of device information for an account.

## Structure

`V2AccountDeviceList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account name. | String getAccountName() | setAccountName(String accountName) |
| `HasMoreData` | `boolean` | Required | Has more device flag? | boolean getHasMoreData() | setHasMoreData(boolean hasMoreData) |
| `LastSeenDeviceId` | `String` | Optional | Last seen device identifier. | String getLastSeenDeviceId() | setLastSeenDeviceId(String lastSeenDeviceId) |
| `MaxPageSize` | `int` | Required | Maximum page size. | int getMaxPageSize() | setMaxPageSize(int maxPageSize) |
| `DeviceList` | [`List<V2AccountDevice>`](../../doc/models/v2-account-device.md) | Required | Account device list. | List<V2AccountDevice> getDeviceList() | setDeviceList(List<V2AccountDevice> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V2AccountDevice;
import com.verizon.thingspace.models.V2AccountDeviceList;
import com.verizon.thingspace.models.V2SoftwareInfo;
import java.util.Arrays;

V2AccountDeviceList v2AccountDeviceList = new V2AccountDeviceList.Builder(
    "0000123456-00001",
    true,
    1000,
    Arrays.asList(
        new V2AccountDevice.Builder(
            "15-digit IMEI",
            "10-digit MDN",
            "Model-A",
            "Verizon",
            true,
            true,
            true,
            "HTTP",
            Arrays.asList(
                new V2SoftwareInfo.Builder(
                    "FOTA_Verizon_Model-A_02To03_HF",
                    "3",
                    "2020-09-08T19:00:51.541Z"
                )
                .build()
            )
        )
        .createTime("2021-06-03 00:03:56.079 +0000 UTC")
        .upgradeTime("2021-06-03 00:03:56.079 +0000 UTC")
        .updateTime("2021-06-03 00:03:56.079 +0000 UTC")
        .refreshTime("2021-06-03 00:03:56.079 +0000 UTC")
        .build(),
        new V2AccountDevice.Builder(
            "15-digit IMEI",
            "10-digit MDN",
            "Model-A",
            "Verizon",
            true,
            true,
            true,
            "HTTP",
            Arrays.asList(
                new V2SoftwareInfo.Builder(
                    "FOTA_Verizon_Model-A_02To03_HF",
                    "3",
                    "2020-09-08T19:00:51.541Z"
                )
                .build()
            )
        )
        .createTime("2021-06-03 00:03:56.079 +0000 UTC")
        .upgradeTime("2021-06-03 00:03:56.079 +0000 UTC")
        .updateTime("2021-06-03 00:03:56.079 +0000 UTC")
        .refreshTime("2021-06-03 00:03:56.079 +0000 UTC")
        .build(),
        new V2AccountDevice.Builder(
            "15-digit IMEI",
            "10-digit MDN",
            "Model-A",
            "Verizon",
            true,
            true,
            true,
            "HTTP",
            Arrays.asList(
                new V2SoftwareInfo.Builder(
                    "FOTA_Verizon_Model-A_02To03_HF",
                    "3",
                    "2020-09-08T19:00:51.541Z"
                )
                .build()
            )
        )
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


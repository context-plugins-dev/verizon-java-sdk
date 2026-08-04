
# Device Extended Diagnostics Request

Request for obtaining device extended diagnostics.

## Structure

`DeviceExtendedDiagnosticsRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | The Verizon billing account that the device belongs to. An account name is usually numeric, and must include any leading zeros. | String getAccountName() | setAccountName(String accountName) |
| `DeviceList` | [`List<DeviceId>`](../../doc/models/device-id.md) | Required | The device for which you want diagnostic information, specified by the device's MDN. | List<DeviceId> getDeviceList() | setDeviceList(List<DeviceId> deviceList) |

## Example

```java
import com.verizon.thingspace.models.DeviceExtendedDiagnosticsRequest;
import com.verizon.thingspace.models.DeviceId;
import java.util.Arrays;

DeviceExtendedDiagnosticsRequest deviceExtendedDiagnosticsRequest = new DeviceExtendedDiagnosticsRequest.Builder(
    "1223334444-00001",
    Arrays.asList(
        new DeviceId.Builder(
            "10-digit MDN",
            "mdn"
        )
        .build()
    )
)
.build();
```


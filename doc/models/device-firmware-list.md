
# Device Firmware List

Device Firmware Information.

## Structure

`DeviceFirmwareList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account name. | String getAccountName() | setAccountName(String accountName) |
| `DeviceFirmwarVersionList` | [`List<DeviceFirmwareVersion>`](../../doc/models/device-firmware-version.md) | Optional | List of device & firmware. | List<DeviceFirmwareVersion> getDeviceFirmwarVersionList() | setDeviceFirmwarVersionList(List<DeviceFirmwareVersion> deviceFirmwarVersionList) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DeviceFirmwareList;
import com.verizon.thingspace.models.DeviceFirmwareVersion;
import java.util.Arrays;

DeviceFirmwareList deviceFirmwareList = new DeviceFirmwareList.Builder(
    "0000123456-00001"
)
.deviceFirmwarVersionList(Arrays.asList(
        new DeviceFirmwareVersion.Builder(
            "15-digit IMEI",
            "SR1.2.0.0-10657"
        )
        .status("FirmwareVersionUpdateSuccess")
        .reason("reason8")
        .firmwareVersionUpdateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .build()
    ))
.build();
```


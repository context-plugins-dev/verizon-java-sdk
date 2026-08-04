
# Device Firmware Version

Device and firmware information.

## Structure

`DeviceFirmwareVersion`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Status` | `String` | Optional | - | String getStatus() | setStatus(String status) |
| `Reason` | `String` | Optional | - | String getReason() | setReason(String reason) |
| `DeviceId` | `String` | Required | Device IMEI. | String getDeviceId() | setDeviceId(String deviceId) |
| `FirmwareVersion` | `String` | Required | Device Firmware Version. | String getFirmwareVersion() | setFirmwareVersion(String firmwareVersion) |
| `FirmwareVersionUpdateTime` | `LocalDateTime` | Optional | - | LocalDateTime getFirmwareVersionUpdateTime() | setFirmwareVersionUpdateTime(LocalDateTime firmwareVersionUpdateTime) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DeviceFirmwareVersion;

DeviceFirmwareVersion deviceFirmwareVersion = new DeviceFirmwareVersion.Builder(
    "15-digit IMEI",
    "SR1.2.0.0-10657"
)
.status("FirmwareVersionUpdateSuccess")
.reason("reason0")
.firmwareVersionUpdateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
.build();
```


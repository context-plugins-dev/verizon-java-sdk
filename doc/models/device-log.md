
# Device Log

Device logging information.

## Structure

`DeviceLog`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | `String` | Required | Device IMEI. | String getDeviceId() | setDeviceId(String deviceId) |
| `LogTime` | `LocalDateTime` | Required | Time of log. | LocalDateTime getLogTime() | setLogTime(LocalDateTime logTime) |
| `LogType` | `String` | Required | Log type (one of SoftwareUpdate, Event, UserNotification, AgentService, Wireless, WirelessWeb, MobileBroadbandModem, WindowsMDM). | String getLogType() | setLogType(String logType) |
| `EventLog` | `String` | Required | Event log. | String getEventLog() | setEventLog(String eventLog) |
| `BinaryLogFileBase64` | `String` | Required | Base64-encoded contents of binary log file. | String getBinaryLogFileBase64() | setBinaryLogFileBase64(String binaryLogFileBase64) |
| `BinaryLogFilename` | `String` | Required | File name of binary log file. | String getBinaryLogFilename() | setBinaryLogFilename(String binaryLogFilename) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DeviceLog;

DeviceLog deviceLog = new DeviceLog.Builder(
    "990013907835573",
    DateTimeHelper.fromRfc8601DateTime("2020-10-22T19:29:50.901Z"),
    "logType4",
    "eventLog0",
    "binaryLogFileBase644",
    "binaryLogFilename0"
)
.build();
```


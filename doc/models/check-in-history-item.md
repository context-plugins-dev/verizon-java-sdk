
# Check In History Item

Check-in history for a device.

## Structure

`CheckInHistoryItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | `String` | Required | Device IMEI. | String getDeviceId() | setDeviceId(String deviceId) |
| `ClientType` | `String` | Required | Type of client. | String getClientType() | setClientType(String clientType) |
| `Result` | `String` | Required | - | String getResult() | setResult(String result) |
| `FailureType` | `String` | Required | - | String getFailureType() | setFailureType(String failureType) |
| `TimeCompleted` | `LocalDateTime` | Required | - | LocalDateTime getTimeCompleted() | setTimeCompleted(LocalDateTime timeCompleted) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.CheckInHistoryItem;

CheckInHistoryItem checkInHistoryItem = new CheckInHistoryItem.Builder(
    "990013907835573",
    "clientType0",
    "result6",
    "failureType6",
    DateTimeHelper.fromRfc8601DateTime("2020-10-22T19:35:07.753Z")
)
.build();
```



# V3 Device Status

Device status.

## Structure

`V3DeviceStatus`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | `String` | Required | Device IMEI. | String getDeviceId() | setDeviceId(String deviceId) |
| `Status` | `String` | Required | Success or failure. | String getStatus() | setStatus(String status) |
| `ResultReason` | `String` | Optional | Result reason. | String getResultReason() | setResultReason(String resultReason) |
| `UpdatedTime` | `LocalDateTime` | Optional | Updated Time. | LocalDateTime getUpdatedTime() | setUpdatedTime(LocalDateTime updatedTime) |
| `RecentAttemptTime` | `LocalDateTime` | Optional | The most recent attempt time. | LocalDateTime getRecentAttemptTime() | setRecentAttemptTime(LocalDateTime recentAttemptTime) |
| `NextAttemptTime` | `LocalDateTime` | Optional | Next attempt time. | LocalDateTime getNextAttemptTime() | setNextAttemptTime(LocalDateTime nextAttemptTime) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.V3DeviceStatus;

V3DeviceStatus v3DeviceStatus = new V3DeviceStatus.Builder(
    "15-digit IMEI",
    "UpgradePending"
)
.resultReason("Upgrade pending, the device upgrade is estimated to be scheduled for 06 Oct 22 18:05 UTC")
.updatedTime(DateTimeHelper.fromRfc8601DateTime("2022-08-05T21:05:27.129Z"))
.recentAttemptTime(DateTimeHelper.fromRfc8601DateTime("2022-10-05T21:05:01.19Z"))
.nextAttemptTime(DateTimeHelper.fromRfc8601DateTime("2022-10-06T18:35:00Z"))
.build();
```


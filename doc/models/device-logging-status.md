
# Device Logging Status

Device logging status information.

## Structure

`DeviceLoggingStatus`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceId` | `String` | Required | Device IMEI. | String getDeviceId() | setDeviceId(String deviceId) |
| `ExpiryDate` | `LocalDate` | Required | The date when device logging expires. | LocalDate getExpiryDate() | setExpiryDate(LocalDate expiryDate) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DeviceLoggingStatus;

DeviceLoggingStatus deviceLoggingStatus = new DeviceLoggingStatus.Builder(
    "990013907835573",
    DateTimeHelper.fromSimpleDate("2020-10-19")
)
.build();
```


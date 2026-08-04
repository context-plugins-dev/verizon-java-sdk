
# Download Time Window

## Structure

`DownloadTimeWindow`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StartTime` | `String` | Optional | Device IMEI list. | String getStartTime() | setStartTime(String startTime) |
| `EndTime` | `String` | Optional | Device IMEI list. | String getEndTime() | setEndTime(String endTime) |

## Example

```java
import com.verizon.thingspace.models.DownloadTimeWindow;

DownloadTimeWindow downloadTimeWindow = new DownloadTimeWindow.Builder()
    .startTime("0")
    .endTime("0")
    .build();
```


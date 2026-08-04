
# Notification Report Request

## Structure

`NotificationReportRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | - | String getAccountName() | setAccountName(String accountName) |
| `RequestType` | `String` | Required | - | String getRequestType() | setRequestType(String requestType) |
| `Devices` | [`List<DeviceList>`](../../doc/models/device-list.md) | Required | - | List<DeviceList> getDevices() | setDevices(List<DeviceList> devices) |
| `MonitorExpirationTime` | `String` | Required | - | String getMonitorExpirationTime() | setMonitorExpirationTime(String monitorExpirationTime) |

## Example

```java
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceList;
import com.verizon.thingspace.models.NotificationReportRequest;
import java.util.Arrays;

NotificationReportRequest notificationReportRequest = new NotificationReportRequest.Builder(
    "0242072320-00001",
    "REACHABLE_FOR_DATA",
    Arrays.asList(
        new DeviceList.Builder()
            .deviceIds(Arrays.asList(
                new DeviceId.Builder(
                    "id0",
                    "kind8"
                )
                .build()
            ))
            .build()
    ),
    "2019-12-02T15:00:00-08:00Z"
)
.build();
```


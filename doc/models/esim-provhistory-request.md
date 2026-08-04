
# ESIM Provhistory Request

## Structure

`ESIMProvhistoryRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | - | String getAccountName() | setAccountName(String accountName) |
| `DeviceFilter` | [`List<DeviceId2>`](../../doc/models/device-id-2.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<DeviceId2> getDeviceFilter() | setDeviceFilter(List<DeviceId2> deviceFilter) |
| `Earliest` | `LocalDateTime` | Optional | - | LocalDateTime getEarliest() | setEarliest(LocalDateTime earliest) |
| `Latest` | `LocalDateTime` | Optional | - | LocalDateTime getLatest() | setLatest(LocalDateTime latest) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DeviceId2;
import com.verizon.thingspace.models.ESIMProvhistoryRequest;
import java.util.Arrays;

ESIMProvhistoryRequest eSIMProvhistoryRequest = new ESIMProvhistoryRequest.Builder()
    .accountName("0000123456-00001")
    .deviceFilter(Arrays.asList(
        new DeviceId2.Builder()
            .id("id4")
            .kind("kind2")
            .build(),
        new DeviceId2.Builder()
            .id("id4")
            .kind("kind2")
            .build(),
        new DeviceId2.Builder()
            .id("id4")
            .kind("kind2")
            .build()
    ))
    .earliest(DateTimeHelper.fromRfc8601DateTime("2021-10-15T04:49:35-00:00"))
    .latest(DateTimeHelper.fromRfc8601DateTime("2021-10-15T04:49:49-00:00"))
    .build();
```


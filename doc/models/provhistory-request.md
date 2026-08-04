
# Provhistory Request

## Structure

`ProvhistoryRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32`, *Pattern*: `^[A-Z a-z 0-9 \-]{3,32}$` | String getAccountName() | setAccountName(String accountName) |
| `DeviceFilter` | [`List<GIODeviceId>`](../../doc/models/gio-device-id.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<GIODeviceId> getDeviceFilter() | setDeviceFilter(List<GIODeviceId> deviceFilter) |
| `Earliest` | `LocalDateTime` | Optional | - | LocalDateTime getEarliest() | setEarliest(LocalDateTime earliest) |
| `Latest` | `LocalDateTime` | Optional | - | LocalDateTime getLatest() | setLatest(LocalDateTime latest) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.GIODeviceId;
import com.verizon.thingspace.models.ProvhistoryRequest;
import java.util.Arrays;

ProvhistoryRequest provhistoryRequest = new ProvhistoryRequest.Builder()
    .accountName("0000123456-00001")
    .deviceFilter(Arrays.asList(
        new GIODeviceId.Builder(
            "kind2",
            "id4"
        )
        .build(),
        new GIODeviceId.Builder(
            "kind2",
            "id4"
        )
        .build(),
        new GIODeviceId.Builder(
            "kind2",
            "id4"
        )
        .build()
    ))
    .earliest(DateTimeHelper.fromRfc8601DateTime("2021-10-15T04:49:35-00:00"))
    .latest(DateTimeHelper.fromRfc8601DateTime("2021-10-15T04:49:49-00:00"))
    .build();
```


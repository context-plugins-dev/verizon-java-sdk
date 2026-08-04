
# Daily Usage Response

## Structure

`DailyUsageResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HasMoreData` | `Boolean` | Optional | A flag set to indicate if there is more than one page of data returned by the query (true) or if only one page of data returned (false) | Boolean getHasMoreData() | setHasMoreData(Boolean hasMoreData) |
| `DeviceId` | [`GIODeviceId`](../../doc/models/gio-device-id.md) | Optional | - | GIODeviceId getDeviceId() | setDeviceId(GIODeviceId deviceId) |
| `UsageHistory` | [`List<DailyUsageHistory>`](../../doc/models/daily-usage-history.md) | Optional | - | List<DailyUsageHistory> getUsageHistory() | setUsageHistory(List<DailyUsageHistory> usageHistory) |

## Example

```java
import com.verizon.thingspace.models.DailyUsageHistory;
import com.verizon.thingspace.models.DailyUsageResponse;
import com.verizon.thingspace.models.ExtendedAttribute;
import com.verizon.thingspace.models.GIODeviceId;
import java.util.Arrays;

DailyUsageResponse dailyUsageResponse = new DailyUsageResponse.Builder()
    .hasMoreData(false)
    .deviceId(new GIODeviceId.Builder(
        "kind8",
        "id0"
    )
    .build())
    .usageHistory(Arrays.asList(
        new DailyUsageHistory.Builder()
            .bytesUsed("bytesUsed2")
            .extendedAttributes(Arrays.asList(
                new ExtendedAttribute.Builder()
                    .key("key8")
                    .value("value0")
                    .build(),
                new ExtendedAttribute.Builder()
                    .key("key8")
                    .value("value0")
                    .build(),
                new ExtendedAttribute.Builder()
                    .key("key8")
                    .value("value0")
                    .build()
            ))
            .servicePlan("servicePlan0")
            .smsUsed("smsUsed6")
            .source("source4")
            .build(),
        new DailyUsageHistory.Builder()
            .bytesUsed("bytesUsed2")
            .extendedAttributes(Arrays.asList(
                new ExtendedAttribute.Builder()
                    .key("key8")
                    .value("value0")
                    .build(),
                new ExtendedAttribute.Builder()
                    .key("key8")
                    .value("value0")
                    .build(),
                new ExtendedAttribute.Builder()
                    .key("key8")
                    .value("value0")
                    .build()
            ))
            .servicePlan("servicePlan0")
            .smsUsed("smsUsed6")
            .source("source4")
            .build()
    ))
    .build();
```


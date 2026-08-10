
# Device Usage List Result

Response to return the daily network data usage of a single device during a specified time period.

## Structure

`DeviceUsageListResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HasMoreData` | `Boolean` | Optional | False for a status 200 response.True for a status 202 response, indicating that there is more data to be retrieved. | Boolean getHasMoreData() | setHasMoreData(Boolean hasMoreData) |
| `UsageHistory` | [`List<Usage>`](../../doc/models/usage.md) | Optional | Placeholder. | List<Usage> getUsageHistory() | setUsageHistory(List<Usage> usageHistory) |

## Example

```java
import com.verizon.thingspace.models.CustomFields;
import com.verizon.thingspace.models.DeviceUsageListResult;
import com.verizon.thingspace.models.Usage;
import java.util.Arrays;

DeviceUsageListResult deviceUsageListResult = new DeviceUsageListResult.Builder()
    .hasMoreData(false)
    .usageHistory(Arrays.asList(
        new Usage.Builder()
            .bytesUsed(4096L)
            .extendedAttributes(Arrays.asList(
                new CustomFields.Builder(
                    "MoSms"
                )
                .value("0")
                .build()
            ))
            .servicePlan("servicePlan0")
            .smsUsed(0)
            .source("Raw Usage")
            .timestamp("2020-12-01T00:00:00Z")
            .build()
    ))
    .build();
```



# Device Provisioning History List Result

Response to return the provisioning history of a specified device during a specified time period.

## Structure

`DeviceProvisioningHistoryListResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HasMoreData` | `Boolean` | Optional | False for a status 200 response.True for a status 202 response, indicating that there is more data to be retrieved. | Boolean getHasMoreData() | setHasMoreData(Boolean hasMoreData) |
| `ProvisioningHistory` | [`List<ProvisioningHistory>`](../../doc/models/provisioning-history.md) | Optional | The provisioning history of a specified device during a specified time period. | List<ProvisioningHistory> getProvisioningHistory() | setProvisioningHistory(List<ProvisioningHistory> provisioningHistory) |

## Example

```java
import com.verizon.thingspace.models.DeviceProvisioningHistoryListResult;
import com.verizon.thingspace.models.ProvisioningHistory;
import java.util.Arrays;

DeviceProvisioningHistoryListResult deviceProvisioningHistoryListResult = new DeviceProvisioningHistoryListResult.Builder()
    .hasMoreData(false)
    .provisioningHistory(Arrays.asList(
        new ProvisioningHistory.Builder()
            .occurredAt("2015-12-17T13:56:13-05:00")
            .status("Success")
            .eventBy("Harry Potter")
            .eventType("Activation Confirmed")
            .mdn("")
            .msisdn("15086303371")
            .servicePlan("Tablet5GB")
            .extendedAttributes(Arrays.asList(

            ))
            .build()
    ))
    .build();
```


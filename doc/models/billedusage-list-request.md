
# Billedusage List Request

Information required to associate a usage segmentation label with a device to retrieve billing.

## Structure

`BilledusageListRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | - | String getAccountName() | setAccountName(String accountName) |
| `Labels` | [`LabelsList`](../../doc/models/labels-list.md) | Optional | - | LabelsList getLabels() | setLabels(LabelsList labels) |
| `DeviceIds` | [`List<DeviceList>`](../../doc/models/device-list.md) | Optional | - | List<DeviceList> getDeviceIds() | setDeviceIds(List<DeviceList> deviceIds) |
| `BillingCycle` | [`BillingCycle`](../../doc/models/billing-cycle.md) | Optional | - | BillingCycle getBillingCycle() | setBillingCycle(BillingCycle billingCycle) |

## Example

```java
import com.verizon.thingspace.models.BilledusageListRequest;
import com.verizon.thingspace.models.BillingCycle;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceLabels;
import com.verizon.thingspace.models.DeviceList;
import com.verizon.thingspace.models.LabelsList;
import com.verizon.thingspace.models.containers.LabelsListDeviceIds;
import java.util.Arrays;

BilledusageListRequest billedusageListRequest = new BilledusageListRequest.Builder(
    "9231221278-99990"
)
.labels(new LabelsList.Builder()
        .deviceIds(Arrays.asList(
            LabelsListDeviceIds.fromDeviceLabels(
                new DeviceLabels.Builder(
                    "name6",
                    "value8"
                )
                .build()
            )
        ))
        .build())
.deviceIds(Arrays.asList(
        new DeviceList.Builder()
            .deviceIds(Arrays.asList(
                new DeviceId.Builder(
                    "id0",
                    "kind8"
                )
                .build(),
                new DeviceId.Builder(
                    "id0",
                    "kind8"
                )
                .build()
            ))
            .build(),
        new DeviceList.Builder()
            .deviceIds(Arrays.asList(
                new DeviceId.Builder(
                    "id0",
                    "kind8"
                )
                .build(),
                new DeviceId.Builder(
                    "id0",
                    "kind8"
                )
                .build()
            ))
            .build()
    ))
.billingCycle(new BillingCycle.Builder()
        .year("year6")
        .month("month4")
        .build())
.build();
```


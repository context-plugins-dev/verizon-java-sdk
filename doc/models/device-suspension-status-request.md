
# Device Suspension Status Request

Request to return service suspension information about one or more devices.

## Structure

`DeviceSuspensionStatusRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIds` | [`List<DeviceId>`](../../doc/models/device-id.md) | Optional | The devices that you want to include in the request, specified by device identifier. You only need to provide one identifier per device. | List<DeviceId> getDeviceIds() | setDeviceIds(List<DeviceId> deviceIds) |
| `Filter` | [`DeviceFilterWithoutAccount`](../../doc/models/device-filter-without-account.md) | Optional | Filter for devices without account. | DeviceFilterWithoutAccount getFilter() | setFilter(DeviceFilterWithoutAccount filter) |
| `AccountName` | `String` | Optional | The name of a billing account. | String getAccountName() | setAccountName(String accountName) |

## Example

```java
import com.verizon.thingspace.models.CustomFields;
import com.verizon.thingspace.models.DeviceFilterWithoutAccount;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceSuspensionStatusRequest;
import java.util.Arrays;

DeviceSuspensionStatusRequest deviceSuspensionStatusRequest = new DeviceSuspensionStatusRequest.Builder()
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
        .build(),
        new DeviceId.Builder(
            "id0",
            "kind8"
        )
        .build()
    ))
    .filter(new DeviceFilterWithoutAccount.Builder()
        .groupName("suspended devices")
        .servicePlan("servicePlan6")
        .customFields(Arrays.asList(
            new CustomFields.Builder(
                "key0"
            )
            .value("value2")
            .build(),
            new CustomFields.Builder(
                "key0"
            )
            .value("value2")
            .build(),
            new CustomFields.Builder(
                "key0"
            )
            .value("value2")
            .build()
        ))
        .build())
    .accountName("1223334444-00001")
    .build();
```


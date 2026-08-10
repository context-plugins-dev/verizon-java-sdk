
# Device Filter

Specify the kind of the device identifier, the type of match, and the string that you want to match.

## Structure

`DeviceFilter`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Account` | `String` | Optional | The the billing account that the devices belong to. | String getAccount() | setAccount(String account) |
| `GroupName` | `String` | Optional | Only include devices that are in this device group. | String getGroupName() | setGroupName(String groupName) |
| `ServicePlan` | `String` | Optional | Only include devices that have this service plan. | String getServicePlan() | setServicePlan(String servicePlan) |
| `CustomFields` | [`List<CustomFields>`](../../doc/models/custom-fields.md) | Optional | Custom field names and values, if you want to only include devices that have matching values. | List<CustomFields> getCustomFields() | setCustomFields(List<CustomFields> customFields) |

## Example

```java
import com.verizon.thingspace.models.CustomFields;
import com.verizon.thingspace.models.DeviceFilter;
import java.util.Arrays;

DeviceFilter deviceFilter = new DeviceFilter.Builder()
    .account("account4")
    .groupName("Short-Haul Trucks")
    .servicePlan("servicePlan6")
    .customFields(Arrays.asList(
        new CustomFields.Builder(
            "CustomField1"
        )
        .value("East Region Trucks")
        .build()
    ))
    .build();
```


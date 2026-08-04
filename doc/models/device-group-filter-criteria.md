
# Device Group Filter Criteria

## Structure

`DeviceGroupFilterCriteria`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FilterCriteria` | [`DeviceGroupFilter`](../../doc/models/device-group-filter.md) | Optional | - | DeviceGroupFilter getFilterCriteria() | setFilterCriteria(DeviceGroupFilter filterCriteria) |

## Example

```java
import com.verizon.thingspace.models.DeviceGroupFilter;
import com.verizon.thingspace.models.DeviceGroupFilterCriteria;

DeviceGroupFilterCriteria deviceGroupFilterCriteria = new DeviceGroupFilterCriteria.Builder()
    .filterCriteria(new DeviceGroupFilter.Builder()
        .deviceGroupName("deviceGroupName4")
        .individualOrCombined("IndividualOrCombined4")
        .accountName("accountName0")
        .build())
    .build();
```


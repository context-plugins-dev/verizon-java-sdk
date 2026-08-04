
# Device Group Object

## Structure

`DeviceGroupObject`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceGroup` | [`DeviceGroupFilterCriteria`](../../doc/models/device-group-filter-criteria.md) | Optional | - | DeviceGroupFilterCriteria getDeviceGroup() | setDeviceGroup(DeviceGroupFilterCriteria deviceGroup) |

## Example

```java
import com.verizon.thingspace.models.DeviceGroupFilter;
import com.verizon.thingspace.models.DeviceGroupFilterCriteria;
import com.verizon.thingspace.models.DeviceGroupObject;

DeviceGroupObject deviceGroupObject = new DeviceGroupObject.Builder()
    .deviceGroup(new DeviceGroupFilterCriteria.Builder()
        .filterCriteria(new DeviceGroupFilter.Builder()
            .deviceGroupName("deviceGroupName4")
            .individualOrCombined("IndividualOrCombined4")
            .accountName("accountName0")
            .build())
        .build())
    .build();
```


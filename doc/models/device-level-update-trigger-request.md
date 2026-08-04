
# Device Level Update Trigger Request

## Structure

`DeviceLevelUpdateTriggerRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TriggerId` | `String` | Optional | The system assigned UUID of the trigger | String getTriggerId() | setTriggerId(String triggerId) |
| `TriggerName` | `String` | Optional | The user defined name of the trigger | String getTriggerName() | setTriggerName(String triggerName) |
| `EcpdId` | `String` | Optional | The Enterprise Customer Profile Database ID | String getEcpdId() | setEcpdId(String ecpdId) |
| `TriggerCategory` | [`TriggerCategoryEnum`](../../doc/models/trigger-category-enum.md) | Optional | The type of trigger being created or modified | TriggerCategoryEnum getTriggerCategory() | setTriggerCategory(TriggerCategoryEnum triggerCategory) |
| `DataTrigger` | [`DataTrigger2`](../../doc/models/data-trigger-2.md) | Optional | - | DataTrigger2 getDataTrigger() | setDataTrigger(DataTrigger2 dataTrigger) |
| `Notification` | [`Notificationarray`](../../doc/models/notificationarray.md) | Optional | - | Notificationarray getNotification() | setNotification(Notificationarray notification) |
| `Active` | [`ActiveEnum`](../../doc/models/active-enum.md) | Optional | A flag to indicate of the trigger is active, true, or not, false | ActiveEnum getActive() | setActive(ActiveEnum active) |

## Example

```java
import com.verizon.thingspace.models.ActiveEnum;
import com.verizon.thingspace.models.ComparitorEnum;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.DataTrigger2;
import com.verizon.thingspace.models.DeviceGroupFilter;
import com.verizon.thingspace.models.DeviceGroupFilterCriteria;
import com.verizon.thingspace.models.DeviceLevelUpdateTriggerRequest;
import com.verizon.thingspace.models.ThresholdUnitEnum;
import com.verizon.thingspace.models.TriggerCategoryEnum;

DeviceLevelUpdateTriggerRequest deviceLevelUpdateTriggerRequest = new DeviceLevelUpdateTriggerRequest.Builder()
    .triggerId("be1b5958-ffff-eeee-gggg-b1b7618c0035")
    .triggerName("name of the trigger")
    .ecpdId("Verizon profile ID")
    .triggerCategory(TriggerCategoryEnum.PRICEPLANDATAUSAGE)
    .dataTrigger(new DataTrigger2.Builder()
        .deviceGroup(new DeviceGroupFilterCriteria.Builder()
            .filterCriteria(new DeviceGroupFilter.Builder()
                .deviceGroupName("deviceGroupName4")
                .individualOrCombined("IndividualOrCombined4")
                .accountName("accountName0")
                .build())
            .build())
        .conditionType(ConditionTypeEnum.AGING)
        .comparitor(ComparitorEnum.EQ)
        .threshold(222)
        .thresholdUnit(ThresholdUnitEnum.MB)
        .build())
    .active(ActiveEnum.ENUM_TRUE)
    .build();
```


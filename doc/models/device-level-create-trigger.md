
# Device Level Create Trigger

## Structure

`DeviceLevelCreateTrigger`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TriggerName` | `String` | Optional | The user defined name of the trigger | String getTriggerName() | setTriggerName(String triggerName) |
| `EcpdId` | `String` | Optional | The Enterprise Customer Profile Database ID | String getEcpdId() | setEcpdId(String ecpdId) |
| `TriggerCategory` | [`TriggerCategoryEnum`](../../doc/models/trigger-category-enum.md) | Optional | The type of trigger being created or modified | TriggerCategoryEnum getTriggerCategory() | setTriggerCategory(TriggerCategoryEnum triggerCategory) |
| `DataTrigger` | [`DataTrigger2`](../../doc/models/data-trigger-2.md) | Optional | - | DataTrigger2 getDataTrigger() | setDataTrigger(DataTrigger2 dataTrigger) |
| `Notification` | [`Notificationarray`](../../doc/models/notificationarray.md) | Optional | - | Notificationarray getNotification() | setNotification(Notificationarray notification) |

## Example

```java
import com.verizon.thingspace.models.ComparitorEnum;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.DataTrigger2;
import com.verizon.thingspace.models.DeviceGroupFilter;
import com.verizon.thingspace.models.DeviceGroupFilterCriteria;
import com.verizon.thingspace.models.DeviceLevelCreateTrigger;
import com.verizon.thingspace.models.Notificationarray;
import com.verizon.thingspace.models.ThresholdUnitEnum;
import com.verizon.thingspace.models.TriggerCategoryEnum;

DeviceLevelCreateTrigger deviceLevelCreateTrigger = new DeviceLevelCreateTrigger.Builder()
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
    .notification(new Notificationarray.Builder()
        .notificationType("notificationType8")
        .callback(false)
        .emailNotification(false)
        .notificationGroupName("notificationGroupName6")
        .notificationFrequencyFactor(22)
        .build())
    .build();
```



# Data Trigger 4

## Structure

`DataTrigger4`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountLevel` | [`AccountLevelObject`](../../doc/models/account-level-object.md) | Optional | - | AccountLevelObject getAccountLevel() | setAccountLevel(AccountLevelObject accountLevel) |
| `DeviceGroup` | [`DeviceGroupFilterCriteria`](../../doc/models/device-group-filter-criteria.md) | Optional | - | DeviceGroupFilterCriteria getDeviceGroup() | setDeviceGroup(DeviceGroupFilterCriteria deviceGroup) |
| `ConditionType` | [`ConditionTypeEnum`](../../doc/models/condition-type-enum.md) | Optional | The condition type being monitored | ConditionTypeEnum getConditionType() | setConditionType(ConditionTypeEnum conditionType) |
| `Comparitor` | [`ComparitorEnum`](../../doc/models/comparitor-enum.md) | Optional | The boolean of the comparison. `gt` is Greater Than, `lt` is Less Than and `eq` is Equal To | ComparitorEnum getComparitor() | setComparitor(ComparitorEnum comparitor) |
| `Threshold` | `Integer` | Optional | The threshold value the trigger monitors for | Integer getThreshold() | setThreshold(Integer threshold) |
| `ThresholdUnit` | [`ThresholdUnitEnum`](../../doc/models/threshold-unit-enum.md) | Optional | The units of the threshold. This can be KB, Kilobits, MB, Megabits, or GB, Gigabits | ThresholdUnitEnum getThresholdUnit() | setThresholdUnit(ThresholdUnitEnum thresholdUnit) |
| `CycleType` | [`RulesCycleTypeEnum`](../../doc/models/rules-cycle-type-enum.md) | Optional | The interval to monitor for the threshold. This can be Daily, Weekly or Monthly | RulesCycleTypeEnum getCycleType() | setCycleType(RulesCycleTypeEnum cycleType) |
| `AllowanceThreshold` | [`AllowanceThreshold`](../../doc/models/allowance-threshold.md) | Optional | - | AllowanceThreshold getAllowanceThreshold() | setAllowanceThreshold(AllowanceThreshold allowanceThreshold) |
| `Action` | [`Actionobject`](../../doc/models/actionobject.md) | Optional | - | Actionobject getAction() | setAction(Actionobject action) |

## Example

```java
import com.verizon.thingspace.models.AccountLevelActionEnum;
import com.verizon.thingspace.models.AccountLevelFilter;
import com.verizon.thingspace.models.AccountLevelObject;
import com.verizon.thingspace.models.Accountnames;
import com.verizon.thingspace.models.ComparitorEnum;
import com.verizon.thingspace.models.ConditionTypeEnum;
import com.verizon.thingspace.models.DataTrigger4;
import com.verizon.thingspace.models.DeviceGroupFilter;
import com.verizon.thingspace.models.DeviceGroupFilterCriteria;
import com.verizon.thingspace.models.RulesCycleTypeEnum;
import com.verizon.thingspace.models.ThresholdUnitEnum;
import com.verizon.thingspace.models.containers.AccountLevelObjectCondition;
import java.util.Arrays;

DataTrigger4 dataTrigger4 = new DataTrigger4.Builder()
    .accountLevel(new AccountLevelObject.Builder()
        .filterCriteria(new AccountLevelFilter.Builder()
            .separateOrCombined("separateOrCombined4")
            .accountNames(new Accountnames.Builder()
                .accountNameList(Arrays.asList(
                    "accountNameList7",
                    "accountNameList8",
                    "accountNameList9"
                ))
                .build())
            .build())
        .condition(AccountLevelObjectCondition.fromConditionType(
            ConditionTypeEnum.INDIVIDUAL
        ))
        .action(AccountLevelActionEnum.SUSPEND)
        .build())
    .deviceGroup(new DeviceGroupFilterCriteria.Builder()
        .filterCriteria(new DeviceGroupFilter.Builder()
            .deviceGroupName("deviceGroupName4")
            .individualOrCombined("IndividualOrCombined4")
            .accountName("accountName0")
            .build())
        .build())
    .conditionType(ConditionTypeEnum.AGING)
    .comparitor(ComparitorEnum.GT)
    .threshold(100)
    .thresholdUnit(ThresholdUnitEnum.KB)
    .cycleType(RulesCycleTypeEnum.DAILY)
    .build();
```


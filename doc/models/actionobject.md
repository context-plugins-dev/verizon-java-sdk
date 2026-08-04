
# Actionobject

## Structure

`Actionobject`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Suspend` | `Boolean` | Optional | - | Boolean getSuspend() | setSuspend(Boolean suspend) |
| `SuspendDetails` | [`Suspenddetailsobject`](../../doc/models/suspenddetailsobject.md) | Optional | - | Suspenddetailsobject getSuspendDetails() | setSuspendDetails(Suspenddetailsobject suspendDetails) |
| `ChangePlan` | `Boolean` | Optional | a flag to set if the trigger changes service plans, true, or not, false | Boolean getChangePlan() | setChangePlan(Boolean changePlan) |
| `ChangePlanDetails` | [`ChangePlanDetails`](../../doc/models/change-plan-details.md) | Optional | The service plan code to switch to | ChangePlanDetails getChangePlanDetails() | setChangePlanDetails(ChangePlanDetails changePlanDetails) |

## Example

```java
import com.verizon.thingspace.models.Actionobject;
import com.verizon.thingspace.models.ChangePlanDetails;
import com.verizon.thingspace.models.Suspenddetailsobject;
import com.verizon.thingspace.models.ThresholdUnitEnum;
import java.util.Arrays;

Actionobject actionobject = new Actionobject.Builder()
    .suspend(true)
    .suspendDetails(new Suspenddetailsobject.Builder()
        .suspendFromAccounts(Arrays.asList(
            "suspendFromAccounts7"
        ))
        .suspendDuration(152)
        .suspendOption("suspendOption2")
        .threshold(166)
        .thresholdUnit(ThresholdUnitEnum.GB)
        .build())
    .changePlan(true)
    .changePlanDetails(new ChangePlanDetails.Builder()
        .toCarrierServicePlanCode("toCarrierServicePlanCode2")
        .build())
    .build();
```



# Action Object Call

## Structure

`ActionObjectCall`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Actionobject`](../../doc/models/actionobject.md) | Optional | - | Actionobject getAction() | setAction(Actionobject action) |

## Example

```java
import com.verizon.thingspace.models.ActionObjectCall;
import com.verizon.thingspace.models.Actionobject;
import com.verizon.thingspace.models.ChangePlanDetails;
import com.verizon.thingspace.models.Suspenddetailsobject;
import com.verizon.thingspace.models.ThresholdUnitEnum;
import java.util.Arrays;

ActionObjectCall actionObjectCall = new ActionObjectCall.Builder()
    .action(new Actionobject.Builder()
        .suspend(false)
        .suspendDetails(new Suspenddetailsobject.Builder()
            .suspendFromAccounts(Arrays.asList(
                "suspendFromAccounts7"
            ))
            .suspendDuration(152)
            .suspendOption("suspendOption2")
            .threshold(166)
            .thresholdUnit(ThresholdUnitEnum.GB)
            .build())
        .changePlan(false)
        .changePlanDetails(new ChangePlanDetails.Builder()
            .toCarrierServicePlanCode("toCarrierServicePlanCode2")
            .build())
        .build())
    .build();
```


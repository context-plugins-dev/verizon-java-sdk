
# Change Plan Details

The service plan code to switch to

## Structure

`ChangePlanDetails`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ToCarrierServicePlanCode` | `String` | Optional | - | String getToCarrierServicePlanCode() | setToCarrierServicePlanCode(String toCarrierServicePlanCode) |

## Example

```java
import com.verizon.thingspace.models.ChangePlanDetails;

ChangePlanDetails changePlanDetails = new ChangePlanDetails.Builder()
    .toCarrierServicePlanCode("toCarrierServicePlanCode2")
    .build();
```


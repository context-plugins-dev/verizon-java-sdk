
# Filter Criteria 1

## Structure

`FilterCriteria1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CarrierServicePlanCode` | `String` | Optional | - | String getCarrierServicePlanCode() | setCarrierServicePlanCode(String carrierServicePlanCode) |
| `AccountNameList` | `List<String>` | Optional | An array of account names | List<String> getAccountNameList() | setAccountNameList(List<String> accountNameList) |

## Example

```java
import com.verizon.thingspace.models.FilterCriteria1;
import java.util.Arrays;

FilterCriteria1 filterCriteria1 = new FilterCriteria1.Builder()
    .carrierServicePlanCode("Service plan code value")
    .accountNameList(Arrays.asList(
        "accountNameList7",
        "accountNameList8"
    ))
    .build();
```


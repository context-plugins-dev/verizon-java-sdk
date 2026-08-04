
# Account Share Filter Criteria 1

## Structure

`AccountShareFilterCriteria1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CarrierServicePlanCode` | `String` | Optional | - | String getCarrierServicePlanCode() | setCarrierServicePlanCode(String carrierServicePlanCode) |
| `AccountNameList` | `List<String>` | Optional | An array of account names | List<String> getAccountNameList() | setAccountNameList(List<String> accountNameList) |

## Example

```java
import com.verizon.thingspace.models.AccountShareFilterCriteria1;
import java.util.Arrays;

AccountShareFilterCriteria1 accountShareFilterCriteria1 = new AccountShareFilterCriteria1.Builder()
    .carrierServicePlanCode("Service plan code value")
    .accountNameList(Arrays.asList(
        "accountNameList3"
    ))
    .build();
```


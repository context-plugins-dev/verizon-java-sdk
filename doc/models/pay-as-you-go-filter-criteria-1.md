
# Pay as You Go Filter Criteria 1

## Structure

`PayAsYouGoFilterCriteria1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CarrierServicePlanCode` | `String` | Optional | - | String getCarrierServicePlanCode() | setCarrierServicePlanCode(String carrierServicePlanCode) |
| `AccountNameList` | `List<String>` | Optional | An array of account names | List<String> getAccountNameList() | setAccountNameList(List<String> accountNameList) |

## Example

```java
import com.verizon.thingspace.models.PayAsYouGoFilterCriteria1;
import java.util.Arrays;

PayAsYouGoFilterCriteria1 payAsYouGoFilterCriteria1 = new PayAsYouGoFilterCriteria1.Builder()
    .carrierServicePlanCode("Service plan code value")
    .accountNameList(Arrays.asList(
        "accountNameList1"
    ))
    .build();
```


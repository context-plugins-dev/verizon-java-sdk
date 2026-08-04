
# Accountnames

## Structure

`Accountnames`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountNameList` | `List<String>` | Optional | - | List<String> getAccountNameList() | setAccountNameList(List<String> accountNameList) |

## Example

```java
import com.verizon.thingspace.models.Accountnames;
import java.util.Arrays;

Accountnames accountnames = new Accountnames.Builder()
    .accountNameList(Arrays.asList(
        "accountNameList1",
        "accountNameList2",
        "accountNameList3"
    ))
    .build();
```


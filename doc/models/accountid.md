
# Accountid

## Structure

`Accountid`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | The numeric name of the account and must include leading zeroes | String getAccountName() | setAccountName(String accountName) |
| `MtasAccountNumber` | `String` | Optional | - | String getMtasAccountNumber() | setMtasAccountNumber(String mtasAccountNumber) |

## Example

```java
import com.verizon.thingspace.models.Accountid;

Accountid accountid = new Accountid.Builder()
    .accountName("0000123456-00001")
    .mtasAccountNumber("0000123456-00001")
    .build();
```



# Service Usage

## Structure

`ServiceUsage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | Account identifier. | String getAccountName() | setAccountName(String accountName) |
| `TransactionsCount` | `String` | Optional | Total requests for the account during the reporting period. | String getTransactionsCount() | setTransactionsCount(String transactionsCount) |

## Example

```java
import com.verizon.thingspace.models.ServiceUsage;

ServiceUsage serviceUsage = new ServiceUsage.Builder()
    .accountName("3333355555-00001")
    .transactionsCount("200")
    .build();
```


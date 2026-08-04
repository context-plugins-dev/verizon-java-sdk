
# Managed Accounts Add Request

## Structure

`ManagedAccountsAddRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account identifier | String getAccountName() | setAccountName(String accountName) |
| `ServiceName` | [`ServiceNameEnum`](../../doc/models/service-name-enum.md) | Required | Service name<br><br>**Default**: `ServiceNameEnum.LOCATION` | ServiceNameEnum getServiceName() | setServiceName(ServiceNameEnum serviceName) |
| `Type` | `String` | Required | SKU name | String getType() | setType(String type) |
| `ManagedAccList` | `List<String>` | Required | managed account list | List<String> getManagedAccList() | setManagedAccList(List<String> managedAccList) |

## Example

```java
import com.verizon.thingspace.models.ManagedAccountsAddRequest;
import com.verizon.thingspace.models.ServiceNameEnum;
import java.util.Arrays;

ManagedAccountsAddRequest managedAccountsAddRequest = new ManagedAccountsAddRequest.Builder(
    "1234567890-00001",
    ServiceNameEnum.LOCATION,
    "TS-LOC-COARSE-CellID-Aggr",
    Arrays.asList(
        "1223334444-00001",
        "2334445555-00001",
        "3445556666-00001"
    )
)
.build();
```


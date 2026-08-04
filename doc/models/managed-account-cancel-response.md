
# Managed Account Cancel Response

## Structure

`ManagedAccountCancelResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Txid` | `String` | Required | Transaction identifier | String getTxid() | setTxid(String txid) |
| `AccountName` | `String` | Required | Managed account identifier | String getAccountName() | setAccountName(String accountName) |
| `PaccountName` | `String` | Required | Primary account identifier | String getPaccountName() | setPaccountName(String paccountName) |
| `ServiceName` | [`ServiceNameEnum`](../../doc/models/service-name-enum.md) | Required | Service name<br><br>**Default**: `ServiceNameEnum.LOCATION` | ServiceNameEnum getServiceName() | setServiceName(ServiceNameEnum serviceName) |
| `Status` | `String` | Required | Deactivate/cancel status, Success or Fail | String getStatus() | setStatus(String status) |
| `Reason` | `String` | Required | Detailed reason | String getReason() | setReason(String reason) |

## Example

```java
import com.verizon.thingspace.models.ManagedAccountCancelResponse;
import com.verizon.thingspace.models.ServiceNameEnum;

ManagedAccountCancelResponse managedAccountCancelResponse = new ManagedAccountCancelResponse.Builder(
    "4fbff332-eeee-ffff-gggg-7e3bdc90bd28",
    "1223334444-00001",
    "1223334444-00001",
    ServiceNameEnum.LOCATION,
    "Success",
    "Success"
)
.build();
```


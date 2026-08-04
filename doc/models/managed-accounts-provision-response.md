
# Managed Accounts Provision Response

## Structure

`ManagedAccountsProvisionResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Txid` | `String` | Optional | Transaction identifier | String getTxid() | setTxid(String txid) |
| `AccountName` | `String` | Optional | Account identifier | String getAccountName() | setAccountName(String accountName) |
| `PaccountName` | `String` | Optional | Primary Account identifier | String getPaccountName() | setPaccountName(String paccountName) |
| `ServiceName` | [`ServiceNameEnum`](../../doc/models/service-name-enum.md) | Optional | Service name<br><br>**Default**: `ServiceNameEnum.LOCATION` | ServiceNameEnum getServiceName() | setServiceName(ServiceNameEnum serviceName) |
| `Status` | `String` | Optional | Provision status. Success or Fail | String getStatus() | setStatus(String status) |
| `Reason` | `String` | Optional | Detailed reason | String getReason() | setReason(String reason) |

## Example

```java
import com.verizon.thingspace.models.ManagedAccountsProvisionResponse;
import com.verizon.thingspace.models.ServiceNameEnum;

ManagedAccountsProvisionResponse managedAccountsProvisionResponse = new ManagedAccountsProvisionResponse.Builder()
    .txid("4fbff332-eeee-ffff-gggg-7e3bdc90bd28")
    .accountName("1223334444-00001")
    .paccountName("1223334444-00001")
    .serviceName(ServiceNameEnum.LOCATION)
    .status("Success")
    .reason("Success")
    .build();
```


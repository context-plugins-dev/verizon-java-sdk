
# Managed Account Cancel Request

## Structure

`ManagedAccountCancelRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Managed account identifier | String getAccountName() | setAccountName(String accountName) |
| `PaccountName` | `String` | Required | Primary Account identifier | String getPaccountName() | setPaccountName(String paccountName) |
| `ServiceName` | [`ServiceNameEnum`](../../doc/models/service-name-enum.md) | Required | Service name<br><br>**Default**: `ServiceNameEnum.LOCATION` | ServiceNameEnum getServiceName() | setServiceName(ServiceNameEnum serviceName) |
| `Type` | `String` | Required | SKU name | String getType() | setType(String type) |
| `Txid` | `String` | Required | Transaction identifier returned by provision request | String getTxid() | setTxid(String txid) |

## Example

```java
import com.verizon.thingspace.models.ManagedAccountCancelRequest;
import com.verizon.thingspace.models.ServiceNameEnum;

ManagedAccountCancelRequest managedAccountCancelRequest = new ManagedAccountCancelRequest.Builder(
    "1223334444-00001",
    "1223334444-00001",
    ServiceNameEnum.LOCATION,
    "TS-LOC-COARSE-CellID-5K",
    "d4fbff33-eeee-ffff-gggg-2c90bd287e3b"
)
.build();
```


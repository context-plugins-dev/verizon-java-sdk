
# Transaction ID

The transaction ID of the request that you want to cancel, from the POST /devicelocations synchronus response.

## Structure

`TransactionID`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Txid` | `String` | Optional | - | String getTxid() | setTxid(String txid) |

## Example

```java
import com.verizon.thingspace.models.TransactionID;

TransactionID transactionID = new TransactionID.Builder()
    .txid("2c90bd28-eeee-ffff-gggg-7e3bd4fbff33")
    .build();
```


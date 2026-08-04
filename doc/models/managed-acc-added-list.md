
# Managed Acc Added List

## Structure

`ManagedAccAddedList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | Account name | String getId() | setId(String id) |
| `Txid` | `String` | Optional | Transaction identifier | String getTxid() | setTxid(String txid) |

## Example

```java
import com.verizon.thingspace.models.ManagedAccAddedList;

ManagedAccAddedList managedAccAddedList = new ManagedAccAddedList.Builder()
    .id("1223334444-00001")
    .txid("2c90bd28-eeee-ffff-gggg-7e3bd4fbff33")
    .build();
```


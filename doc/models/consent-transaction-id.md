
# Consent Transaction ID

The transaction ID of the request that you want to cancel, from the POST /devicelocations synchronus response.

## Structure

`ConsentTransactionID`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TransactionId` | `String` | Optional | - | String getTransactionId() | setTransactionId(String transactionId) |
| `Status` | `String` | Optional | - | String getStatus() | setStatus(String status) |

## Example

```java
import com.verizon.thingspace.models.ConsentTransactionID;

ConsentTransactionID consentTransactionID = new ConsentTransactionID.Builder()
    .transactionId("2c90bd28-eeee-ffff-gggg-7e3bd4fbff33")
    .status("QUEUED")
    .build();
```


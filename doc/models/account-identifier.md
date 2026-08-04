
# Account Identifier

The ID of the authenticating billing account, in the format `{"billingaccountid":"1234567890-12345"}`.

## Structure

`AccountIdentifier`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Billingaccountid` | `String` | Optional | - | String getBillingaccountid() | setBillingaccountid(String billingaccountid) |

## Example

```java
import com.verizon.thingspace.models.AccountIdentifier;

AccountIdentifier accountIdentifier = new AccountIdentifier.Builder()
    .billingaccountid("0000000000-00001")
    .build();
```


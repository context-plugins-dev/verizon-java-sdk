
# Generate External ID Request

Authenticating account ID.

## Structure

`GenerateExternalIDRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountidentifier` | [`AccountIdentifier`](../../doc/models/account-identifier.md) | Optional | The ID of the authenticating billing account, in the format `{"billingaccountid":"1234567890-12345"}`. | AccountIdentifier getAccountidentifier() | setAccountidentifier(AccountIdentifier accountidentifier) |

## Example

```java
import com.verizon.thingspace.models.AccountIdentifier;
import com.verizon.thingspace.models.GenerateExternalIDRequest;

GenerateExternalIDRequest generateExternalIDRequest = new GenerateExternalIDRequest.Builder()
    .accountidentifier(new AccountIdentifier.Builder()
        .billingaccountid("0000000000-00001")
        .build())
    .build();
```


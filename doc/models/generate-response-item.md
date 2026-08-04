
# Generate Response Item

## Structure

`GenerateResponseItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Imei` | `String` | Optional | - | String getImei() | setImei(String imei) |
| `Credential` | [`GenerateResponseItemCredential`](../../doc/models/generate-response-item-credential.md) | Optional | - | GenerateResponseItemCredential getCredential() | setCredential(GenerateResponseItemCredential credential) |

## Example

```java
import com.verizon.thingspace.models.GenerateResponseItem;
import com.verizon.thingspace.models.GenerateResponseItemCredential;

GenerateResponseItem generateResponseItem = new GenerateResponseItem.Builder()
    .imei("100096454851324")
    .credential(new GenerateResponseItemCredential.Builder()
        .username("username6")
        .password("password0")
        .build())
    .build();
```


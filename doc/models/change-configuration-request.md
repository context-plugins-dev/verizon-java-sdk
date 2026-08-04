
# Change Configuration Request

The request body identifies the device and the values to set.

## Structure

`ChangeConfigurationRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountidentifier` | [`AccountIdentifier`](../../doc/models/account-identifier.md) | Optional | The ID of the authenticating billing account, in the format `{"billingaccountid":"1234567890-12345"}`. | AccountIdentifier getAccountidentifier() | setAccountidentifier(AccountIdentifier accountidentifier) |
| `Resourceidentifier` | [`ResourceIdentifier`](../../doc/models/resource-identifier.md) | Optional | The ID of the target to delete, in the format {"id": "dd1682d3-2d80-cefc-f3ee-25154800beff"}. | ResourceIdentifier getResourceidentifier() | setResourceidentifier(ResourceIdentifier resourceidentifier) |
| `Configuration` | [`Configuration`](../../doc/models/configuration.md) | Optional | List of the field names and values to set. | Configuration getConfiguration() | setConfiguration(Configuration configuration) |

## Example

```java
import com.verizon.thingspace.models.AccountIdentifier;
import com.verizon.thingspace.models.ChangeConfigurationRequest;
import com.verizon.thingspace.models.Configuration;
import com.verizon.thingspace.models.ResourceIdentifier;

ChangeConfigurationRequest changeConfigurationRequest = new ChangeConfigurationRequest.Builder()
    .accountidentifier(new AccountIdentifier.Builder()
        .billingaccountid("1223334444-00001")
        .build())
    .resourceidentifier(new ResourceIdentifier.Builder()
        .id("f8b112df-739c-6236-f059-106c67bafd99")
        .imei("imei2")
        .build())
    .configuration(new Configuration.Builder()
        .frequency("Low")
        .build())
    .build();
```


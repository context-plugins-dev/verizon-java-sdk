
# Delete Target Request

Target to delete.

## Structure

`DeleteTargetRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountidentifier` | [`AccountIdentifier`](../../doc/models/account-identifier.md) | Optional | The ID of the authenticating billing account, in the format `{"billingaccountid":"1234567890-12345"}`. | AccountIdentifier getAccountidentifier() | setAccountidentifier(AccountIdentifier accountidentifier) |
| `Resourceidentifier` | [`ResourceIdentifier`](../../doc/models/resource-identifier.md) | Optional | The ID of the target to delete, in the format {"id": "dd1682d3-2d80-cefc-f3ee-25154800beff"}. | ResourceIdentifier getResourceidentifier() | setResourceidentifier(ResourceIdentifier resourceidentifier) |

## Example

```java
import com.verizon.thingspace.models.AccountIdentifier;
import com.verizon.thingspace.models.DeleteTargetRequest;
import com.verizon.thingspace.models.ResourceIdentifier;

DeleteTargetRequest deleteTargetRequest = new DeleteTargetRequest.Builder()
    .accountidentifier(new AccountIdentifier.Builder()
        .billingaccountid("0000000000-00001")
        .build())
    .resourceidentifier(new ResourceIdentifier.Builder()
        .id("2e61a17d-8fd1-6816-e995-e4c2528bf535")
        .imei("imei2")
        .build())
    .build();
```


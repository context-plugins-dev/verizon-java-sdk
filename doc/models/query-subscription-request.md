
# Query Subscription Request

Fields and values to match.

## Structure

`QuerySubscriptionRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountidentifier` | [`AccountIdentifier`](../../doc/models/account-identifier.md) | Optional | The ID of the authenticating billing account, in the format `{"billingaccountid":"1234567890-12345"}`. | AccountIdentifier getAccountidentifier() | setAccountidentifier(AccountIdentifier accountidentifier) |
| `Selection` | `Map<String, String>` | Optional | A comma-separated list of properties and comparator values to match against subscriptions in the ThingSpace account. See Working with Query Filters for more information. If the request does not include `$selection`, the response will include all subscriptions to which the requesting user has access. | Map<String, String> getSelection() | setSelection(Map<String, String> selection) |
| `Resourceidentifier` | [`ResourceIdentifier`](../../doc/models/resource-identifier.md) | Optional | The ID of the target to delete, in the format {"id": "dd1682d3-2d80-cefc-f3ee-25154800beff"}. | ResourceIdentifier getResourceidentifier() | setResourceidentifier(ResourceIdentifier resourceidentifier) |

## Example

```java
import com.verizon.thingspace.models.AccountIdentifier;
import com.verizon.thingspace.models.QuerySubscriptionRequest;
import com.verizon.thingspace.models.ResourceIdentifier;
import java.util.LinkedHashMap;

QuerySubscriptionRequest querySubscriptionRequest = new QuerySubscriptionRequest.Builder()
    .accountidentifier(new AccountIdentifier.Builder()
        .billingaccountid("1223334444-00001")
        .build())
    .selection(new LinkedHashMap<String, String>() {{
        put("key0", "$selection1");
    }})
    .resourceidentifier(new ResourceIdentifier.Builder()
        .id("dd1682d3-2d80-cefc-f3ee-25154800beff")
        .imei("imei2")
        .build())
    .build();
```



# Search Device Event History Request

Search Device By Property resource definition.

## Structure

`SearchDeviceEventHistoryRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountidentifier` | [`AccountIdentifier`](../../doc/models/account-identifier.md) | Required | The ID of the authenticating billing account, in the format `{"billingaccountid":"1234567890-12345"}`. | AccountIdentifier getAccountidentifier() | setAccountidentifier(AccountIdentifier accountidentifier) |
| `Selection` | `Map<String, String>` | Optional | A comma-separated list of properties and comparator values to match against subscriptions in the ThingSpace account. See Working with Query Filters for more information. If the request does not include `$selection`, the response will include all subscriptions to which the requesting user has access. | Map<String, String> getSelection() | setSelection(Map<String, String> selection) |
| `Resourceidentifier` | [`ResourceIdentifier`](../../doc/models/resource-identifier.md) | Required | The ID of the target to delete, in the format {"id": "dd1682d3-2d80-cefc-f3ee-25154800beff"}. | ResourceIdentifier getResourceidentifier() | setResourceidentifier(ResourceIdentifier resourceidentifier) |
| `Limitnumber` | `Integer` | Optional | The maximum number of events to include in the response. | Integer getLimitnumber() | setLimitnumber(Integer limitnumber) |
| `Page` | `String` | Optional | The maximum number of events to include in the response. | String getPage() | setPage(String page) |

## Example

```java
import com.verizon.thingspace.models.AccountIdentifier;
import com.verizon.thingspace.models.ResourceIdentifier;
import com.verizon.thingspace.models.SearchDeviceEventHistoryRequest;
import java.util.LinkedHashMap;

SearchDeviceEventHistoryRequest searchDeviceEventHistoryRequest = new SearchDeviceEventHistoryRequest.Builder(
    new AccountIdentifier.Builder()
        .billingaccountid("0000000000-00001")
        .build(),
    new ResourceIdentifier.Builder()
        .id("2e61a17d-8fd1-6816-e995-e4c2528bf535")
        .imei("imei2")
        .build()
)
.selection(new LinkedHashMap<String, String>() {{
        put("addressscheme", "streamawsiot");
    }})
.limitnumber(2)
.page("$page6")
.build();
```


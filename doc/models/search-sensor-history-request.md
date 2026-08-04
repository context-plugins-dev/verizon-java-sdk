
# Search Sensor History Request

Search Device By Property resource definition.

## Structure

`SearchSensorHistoryRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountidentifier` | [`AccountIdentifier`](../../doc/models/account-identifier.md) | Required | The ID of the authenticating billing account, in the format `{"billingaccountid":"1234567890-12345"}`. | AccountIdentifier getAccountidentifier() | setAccountidentifier(AccountIdentifier accountidentifier) |
| `Resourceidentifier` | [`ResourceIdentifier`](../../doc/models/resource-identifier.md) | Required | The ID of the target to delete, in the format {"id": "dd1682d3-2d80-cefc-f3ee-25154800beff"}. | ResourceIdentifier getResourceidentifier() | setResourceidentifier(ResourceIdentifier resourceidentifier) |
| `Limitnumber` | `Integer` | Optional | The maximum number of events to include in the response. | Integer getLimitnumber() | setLimitnumber(Integer limitnumber) |
| `Page` | `String` | Optional | The maximum number of events to include in the response. | String getPage() | setPage(String page) |

## Example

```java
import com.verizon.thingspace.models.AccountIdentifier;
import com.verizon.thingspace.models.ResourceIdentifier;
import com.verizon.thingspace.models.SearchSensorHistoryRequest;

SearchSensorHistoryRequest searchSensorHistoryRequest = new SearchSensorHistoryRequest.Builder(
    new AccountIdentifier.Builder()
        .billingaccountid("0000000000-00001")
        .build(),
    new ResourceIdentifier.Builder()
        .id("2e61a17d-8fd1-6816-e995-e4c2528bf535")
        .imei("imei2")
        .build()
)
.limitnumber(2)
.page("$page0")
.build();
```


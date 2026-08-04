
# Dto List Rules Request

## Structure

`DtoListRulesRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Filter` | [`DtoFilter`](../../doc/models/dto-filter.md) | Optional | - | DtoFilter getFilter() | setFilter(DtoFilter filter) |
| `Resourceidentifier` | [`DtoResourceidentifier`](../../doc/models/dto-resourceidentifier.md) | Optional | - | DtoResourceidentifier getResourceidentifier() | setResourceidentifier(DtoResourceidentifier resourceidentifier) |

## Example

```java
import com.verizon.thingspace.models.DtoFilter;
import com.verizon.thingspace.models.DtoListRulesRequest;
import com.verizon.thingspace.models.DtoResourceidentifier;

DtoListRulesRequest dtoListRulesRequest = new DtoListRulesRequest.Builder()
    .accountname("0000123456-00001")
    .filter(new DtoFilter.Builder()
        .expand("$expand0")
        .limitnumber(100)
        .nopagination(false)
        .page("$page0")
        .pagenumber(64)
        .build())
    .resourceidentifier(new DtoResourceidentifier.Builder()
        .id("id4")
        .build())
    .build();
```


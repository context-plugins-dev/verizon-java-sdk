
# Dto List User Request

## Structure

`DtoListUserRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Filter` | [`DtoFilter`](../../doc/models/dto-filter.md) | Optional | - | DtoFilter getFilter() | setFilter(DtoFilter filter) |

## Example

```java
import com.verizon.thingspace.models.DtoFilter;
import com.verizon.thingspace.models.DtoListUserRequest;

DtoListUserRequest dtoListUserRequest = new DtoListUserRequest.Builder()
    .accountname("0000123456-00001")
    .filter(new DtoFilter.Builder()
        .expand("$expand0")
        .limitnumber(100)
        .nopagination(false)
        .page("$page0")
        .pagenumber(64)
        .build())
    .build();
```


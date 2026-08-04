
# Dto Patch Smart Alert Request

## Structure

`DtoPatchSmartAlertRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Resourceidentifier` | [`DtoResourceidentifier`](../../doc/models/dto-resourceidentifier.md) | Optional | - | DtoResourceidentifier getResourceidentifier() | setResourceidentifier(DtoResourceidentifier resourceidentifier) |
| `Smartalert` | [`UserSmartAlert`](../../doc/models/user-smart-alert.md) | Optional | - | UserSmartAlert getSmartalert() | setSmartalert(UserSmartAlert smartalert) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DtoPatchSmartAlertRequest;
import com.verizon.thingspace.models.DtoResourceidentifier;
import com.verizon.thingspace.models.UserSmartAlert;

DtoPatchSmartAlertRequest dtoPatchSmartAlertRequest = new DtoPatchSmartAlertRequest.Builder()
    .accountname("0000123456-00001")
    .resourceidentifier(new DtoResourceidentifier.Builder()
        .id("id4")
        .build())
    .smartalert(new UserSmartAlert.Builder(
        DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
        DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
        "versionid2"
    )
    .accountclientid("accountclientid6")
    .billingaccountid("billingaccountid6")
    .category("category8")
    .condition(154)
    .description("description0")
    .build())
    .build();
```


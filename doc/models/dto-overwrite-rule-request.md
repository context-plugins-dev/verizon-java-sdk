
# Dto Overwrite Rule Request

## Structure

`DtoOverwriteRuleRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Resourceidentifier` | [`DtoResourceidentifier`](../../doc/models/dto-resourceidentifier.md) | Optional | - | DtoResourceidentifier getResourceidentifier() | setResourceidentifier(DtoResourceidentifier resourceidentifier) |
| `Rule` | [`ResourceRule`](../../doc/models/resource-rule.md) | Optional | - | ResourceRule getRule() | setRule(ResourceRule rule) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DtoOverwriteRuleRequest;
import com.verizon.thingspace.models.DtoResourceidentifier;
import com.verizon.thingspace.models.ResourceRule;
import java.io.IOException;

DtoOverwriteRuleRequest dtoOverwriteRuleRequest = new DtoOverwriteRuleRequest.Builder()
    .accountname("0000123456-00001")
    .resourceidentifier(new DtoResourceidentifier.Builder()
        .id("id4")
        .build())
    .rule(new ResourceRule.Builder(
        DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
        "foreignid8",
        DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        "versionid2"
    )
    .accountclientid("accountclientid4")
    .billingaccountid("billingaccountid6")
    .description("description0")
    .deviceid("deviceid0")
    .disabled(false)
    .build())
    .build();
```


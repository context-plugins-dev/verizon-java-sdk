
# Associate Label Request

## Structure

`AssociateLabelRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | The name of a billing account. An account name is usually numeric, and must include any leading zeros. | String getAccountName() | setAccountName(String accountName) |
| `Labels` | [`AccountLabels`](../../doc/models/account-labels.md) | Required | Maximum of 2,000 objects are allowed in the array. | AccountLabels getLabels() | setLabels(AccountLabels labels) |

## Example

```java
import com.verizon.thingspace.models.AccountLabels;
import com.verizon.thingspace.models.AssociateLabelRequest;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceLabels;
import com.verizon.thingspace.models.DeviceList;
import java.util.Arrays;

AssociateLabelRequest associateLabelRequest = new AssociateLabelRequest.Builder(
    "1223334444-00001",
    new AccountLabels.Builder(
        Arrays.asList(
            new DeviceList.Builder()
                .deviceIds(Arrays.asList(
                    new DeviceId.Builder(
                        "id0",
                        "kind8"
                    )
                    .build()
                ))
                .build()
        )
    )
    .label(Arrays.asList(
            new DeviceLabels.Builder(
                "name0",
                "value2"
            )
            .build(),
            new DeviceLabels.Builder(
                "name0",
                "value2"
            )
            .build(),
            new DeviceLabels.Builder(
                "name0",
                "value2"
            )
            .build()
        ))
    .build()
)
.build();
```


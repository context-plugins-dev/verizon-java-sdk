
# Generate Response

## Structure

`GenerateResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Items` | [`List<GenerateResponseItem>`](../../doc/models/generate-response-item.md) | Optional | - | List<GenerateResponseItem> getItems() | setItems(List<GenerateResponseItem> items) |

## Example

```java
import com.verizon.thingspace.models.GenerateResponse;
import com.verizon.thingspace.models.GenerateResponseItem;
import com.verizon.thingspace.models.GenerateResponseItemCredential;
import java.util.Arrays;

GenerateResponse generateResponse = new GenerateResponse.Builder()
    .items(Arrays.asList(
        new GenerateResponseItem.Builder()
            .imei("imei8")
            .credential(new GenerateResponseItemCredential.Builder()
                .username("username6")
                .password("password0")
                .build())
            .build(),
        new GenerateResponseItem.Builder()
            .imei("imei8")
            .credential(new GenerateResponseItemCredential.Builder()
                .username("username6")
                .password("password0")
                .build())
            .build(),
        new GenerateResponseItem.Builder()
            .imei("imei8")
            .credential(new GenerateResponseItemCredential.Builder()
                .username("username6")
                .password("password0")
                .build())
            .build()
    ))
    .build();
```


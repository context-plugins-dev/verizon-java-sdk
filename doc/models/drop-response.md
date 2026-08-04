
# Drop Response

## Structure

`DropResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Items` | [`List<DropResponseItem>`](../../doc/models/drop-response-item.md) | Optional | - | List<DropResponseItem> getItems() | setItems(List<DropResponseItem> items) |

## Example

```java
import com.verizon.thingspace.models.DropResponse;
import com.verizon.thingspace.models.DropResponseItem;
import java.util.Arrays;

DropResponse dropResponse = new DropResponse.Builder()
    .items(Arrays.asList(
        new DropResponseItem.Builder()
            .imei("imei8")
            .build(),
        new DropResponseItem.Builder()
            .imei("imei8")
            .build()
    ))
    .build();
```


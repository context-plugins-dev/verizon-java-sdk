
# Retrieve Response

## Structure

`RetrieveResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Items` | [`List<RetrieveResponseItem>`](../../doc/models/retrieve-response-item.md) | Optional | - | List<RetrieveResponseItem> getItems() | setItems(List<RetrieveResponseItem> items) |

## Example

```java
import com.verizon.thingspace.models.RetrieveResponse;
import com.verizon.thingspace.models.RetrieveResponseItem;
import java.util.Arrays;

RetrieveResponse retrieveResponse = new RetrieveResponse.Builder()
    .items(Arrays.asList(
        new RetrieveResponseItem.Builder()
            .imei("imei8")
            .username("username2")
            .failure("failure8")
            .build()
    ))
    .build();
```


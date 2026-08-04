
# ITIS Item Wrapper

A wrapper carrying an ITIS code item.

## Structure

`ITISItemWrapper`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Item` | [`ITISItemContent`](../../doc/models/itis-item-content.md) | Required | An item object wrapping an ITIS code value. | ITISItemContent getItem() | setItem(ITISItemContent item) |

## Example

```java
import com.verizon.thingspace.models.ITISItemContent;
import com.verizon.thingspace.models.ITISItemWrapper;

ITISItemWrapper iTISItemWrapper = new ITISItemWrapper.Builder(
    new ITISItemContent.Builder(
        10
    )
    .build()
)
.build();
```


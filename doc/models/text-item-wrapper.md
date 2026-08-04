
# Text Item Wrapper

A wrapper carrying a text item.

## Structure

`TextItemWrapper`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Item` | [`TextItemContent`](../../doc/models/text-item-content.md) | Required | An item object wrapping a text value. | TextItemContent getItem() | setItem(TextItemContent item) |

## Example

```java
import com.verizon.thingspace.models.TextItemContent;
import com.verizon.thingspace.models.TextItemWrapper;

TextItemWrapper textItemWrapper = new TextItemWrapper.Builder(
    new TextItemContent.Builder(
        "text2"
    )
    .build()
)
.build();
```


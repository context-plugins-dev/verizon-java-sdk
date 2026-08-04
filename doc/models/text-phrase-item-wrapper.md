
# Text Phrase Item Wrapper

A wrapper carrying a text phrase item.

## Structure

`TextPhraseItemWrapper`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Item` | [`TextPhraseItemContent`](../../doc/models/text-phrase-item-content.md) | Required | An item object wrapping a text phrase value. | TextPhraseItemContent getItem() | setItem(TextPhraseItemContent item) |

## Example

```java
import com.verizon.thingspace.models.TextPhraseItemContent;
import com.verizon.thingspace.models.TextPhraseItemWrapper;

TextPhraseItemWrapper textPhraseItemWrapper = new TextPhraseItemWrapper.Builder(
    new TextPhraseItemContent.Builder(
        "text2"
    )
    .build()
)
.build();
```



# Text Item Content

An item object wrapping a text value.

## Structure

`TextItemContent`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Text` | `String` | Required | Simple text used with ITIS codes. (Text taken from SAE J2540.)<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `500`, *Pattern*: ``^[\w\+\-!()\`\[\]{=};\"':,.\/<>?\|\s]+$`` | String getText() | setText(String text) |

## Example

```java
import com.verizon.thingspace.models.TextItemContent;

TextItemContent textItemContent = new TextItemContent.Builder(
    "text0"
)
.build();
```


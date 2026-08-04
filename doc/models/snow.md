
# Snow

Indicates the surface of the roadway is snow.

## Structure

`Snow`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type13Enum`](../../doc/models/type-13-enum.md) | Optional | Indicates the type of snow. | Type13Enum getType() | setType(Type13Enum type) |

## Example

```java
import com.verizon.thingspace.models.Snow;
import com.verizon.thingspace.models.Type13Enum;

Snow snow = new Snow.Builder()
    .type(Type13Enum.PACKED)
    .build();
```


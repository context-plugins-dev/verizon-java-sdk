
# Grass

Indicates the surface of the roadway is grass.

## Structure

`Grass`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type9Enum`](../../doc/models/type-9-enum.md) | Optional | Indicates the surface of the roadway is grass with low speed limit. | Type9Enum getType() | setType(Type9Enum type) |

## Example

```java
import com.verizon.thingspace.models.Grass;
import com.verizon.thingspace.models.Type9Enum;

Grass grass = new Grass.Builder()
    .type(Type9Enum.LESSTHAN30MPH)
    .build();
```


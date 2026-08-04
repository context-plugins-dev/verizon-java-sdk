
# Cinders

Indicates the surface of the roadway is cinders.

## Structure

`Cinders`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type10Enum`](../../doc/models/type-10-enum.md) | Optional | Indicates the type of cinders. | Type10Enum getType() | setType(Type10Enum type) |

## Example

```java
import com.verizon.thingspace.models.Cinders;
import com.verizon.thingspace.models.Type10Enum;

Cinders cinders = new Cinders.Builder()
    .type(Type10Enum.PACKED)
    .build();
```


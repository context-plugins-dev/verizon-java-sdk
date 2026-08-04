
# Ice

Indicates the surface of the roadway is ice.

## Structure

`Ice`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type12Enum`](../../doc/models/type-12-enum.md) | Optional | Indicates the type of ice. | Type12Enum getType() | setType(Type12Enum type) |

## Example

```java
import com.verizon.thingspace.models.Ice;
import com.verizon.thingspace.models.Type12Enum;

Ice ice = new Ice.Builder()
    .type(Type12Enum.SMOOTH)
    .build();
```


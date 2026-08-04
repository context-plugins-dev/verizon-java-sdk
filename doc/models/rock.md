
# Rock

Indicates the surface of the roadway is rock.

## Structure

`Rock`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type11Enum`](../../doc/models/type-11-enum.md) | Optional | Indicates the type of rock. | Type11Enum getType() | setType(Type11Enum type) |

## Example

```java
import com.verizon.thingspace.models.Rock;
import com.verizon.thingspace.models.Type11Enum;

Rock rock = new Rock.Builder()
    .type(Type11Enum.CRUSHED)
    .build();
```


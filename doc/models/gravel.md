
# Gravel

Indicates the surface of the roadway is gravel.

## Structure

`Gravel`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type8Enum`](../../doc/models/type-8-enum.md) | Optional | Indicates the type of gravel. | Type8Enum getType() | setType(Type8Enum type) |

## Example

```java
import com.verizon.thingspace.models.Gravel;
import com.verizon.thingspace.models.Type8Enum;

Gravel gravel = new Gravel.Builder()
    .type(Type8Enum.PACKEDOILED)
    .build();
```


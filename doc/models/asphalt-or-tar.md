
# Asphalt or Tar

Indicates the surface of the roadway is asphalt or tar.

## Structure

`AsphaltOrTar`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type7Enum`](../../doc/models/type-7-enum.md) | Optional | Indicates the type of asphalt or tar. | Type7Enum getType() | setType(Type7Enum type) |

## Example

```java
import com.verizon.thingspace.models.AsphaltOrTar;
import com.verizon.thingspace.models.Type7Enum;

AsphaltOrTar asphaltOrTar = new AsphaltOrTar.Builder()
    .type(Type7Enum.NEWSHARP)
    .build();
```


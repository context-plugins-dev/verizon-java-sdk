
# Description of Road Surface Asphalt or Tar

## Structure

`DescriptionOfRoadSurfaceAsphaltOrTar`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AsphaltOrTar` | [`AsphaltOrTar`](../../doc/models/asphalt-or-tar.md) | Required | Indicates the surface of the roadway is asphalt or tar. | AsphaltOrTar getAsphaltOrTar() | setAsphaltOrTar(AsphaltOrTar asphaltOrTar) |

## Example

```java
import com.verizon.thingspace.models.AsphaltOrTar;
import com.verizon.thingspace.models.DescriptionOfRoadSurfaceAsphaltOrTar;
import com.verizon.thingspace.models.Type7Enum;

DescriptionOfRoadSurfaceAsphaltOrTar descriptionOfRoadSurfaceAsphaltOrTar = new DescriptionOfRoadSurfaceAsphaltOrTar.Builder(
    new AsphaltOrTar.Builder()
        .type(Type7Enum.NEWSHARP)
        .build()
)
.build();
```


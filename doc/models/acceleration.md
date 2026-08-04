
# Acceleration

## Structure

`Acceleration`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `X` | `String` | Optional | - | String getX() | setX(String x) |
| `Y` | `String` | Optional | - | String getY() | setY(String y) |
| `Z` | `String` | Optional | - | String getZ() | setZ(String z) |

## Example

```java
import com.verizon.thingspace.models.Acceleration;

Acceleration acceleration = new Acceleration.Builder()
    .x("0.0277")
    .y("-1.0334")
    .z("-0.0134")
    .build();
```


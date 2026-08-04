
# Heading Range

Acceptable heading range for road users in degrees.

## Structure

`HeadingRange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Min` | `double` | Required | The minimum value of heading in unit of degrees.<br><br>**Constraints**: `>= 0`, `<= 360` | double getMin() | setMin(double min) |
| `Max` | `double` | Required | The maximum value of heading in unit of degrees.<br><br>**Constraints**: `>= 0`, `<= 360` | double getMax() | setMax(double max) |

## Example

```java
import com.verizon.thingspace.models.HeadingRange;

HeadingRange headingRange = new HeadingRange.Builder(
    174.44D,
    247.86D
)
.build();
```


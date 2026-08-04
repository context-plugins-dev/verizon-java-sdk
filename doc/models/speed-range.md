
# Speed Range

Acceptable speed range for road users in m/s.

## Structure

`SpeedRange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Min` | `double` | Required | The minimum required speed in m/s.<br><br>**Constraints**: `>= 0`, `<= 160` | double getMin() | setMin(double min) |
| `Max` | `double` | Required | The maximum acceptable speed in m/s.<br><br>**Constraints**: `>= 0`, `<= 160` | double getMax() | setMax(double max) |

## Example

```java
import com.verizon.thingspace.models.SpeedRange;

SpeedRange speedRange = new SpeedRange.Builder(
    89.68D,
    160D
)
.build();
```


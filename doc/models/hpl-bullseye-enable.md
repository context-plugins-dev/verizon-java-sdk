
# Hpl Bullseye Enable

A flag that shows if Hyper Precise is enabled (true) or disabled (false).

## Structure

`HplBullseyeEnable`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BullseyeEnable` | `Boolean` | Optional | - | Boolean getBullseyeEnable() | setBullseyeEnable(Boolean bullseyeEnable) |

## Example

```java
import com.verizon.thingspace.models.HplBullseyeEnable;

HplBullseyeEnable hplBullseyeEnable = new HplBullseyeEnable.Builder()
    .bullseyeEnable(true)
    .build();
```


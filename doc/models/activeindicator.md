
# Activeindicator

## Structure

`Activeindicator`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Active` | [`ActiveEnum`](../../doc/models/active-enum.md) | Optional | A flag to indicate of the trigger is active, true, or not, false | ActiveEnum getActive() | setActive(ActiveEnum active) |

## Example

```java
import com.verizon.thingspace.models.ActiveEnum;
import com.verizon.thingspace.models.Activeindicator;

Activeindicator activeindicator = new Activeindicator.Builder()
    .active(ActiveEnum.ENUM_TRUE)
    .build();
```


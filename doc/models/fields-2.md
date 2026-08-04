
# Fields 2

List of fields affected by the event.

## Structure

`Fields2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Temperature` | `String` | Optional | - | String getTemperature() | setTemperature(String temperature) |

## Example

```java
import com.verizon.thingspace.models.Fields2;

Fields2 fields2 = new Fields2.Builder()
    .temperature("18.4")
    .build();
```


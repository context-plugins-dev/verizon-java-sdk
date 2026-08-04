
# Configuration

List of the field names and values to set.

## Structure

`Configuration`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Frequency` | `String` | Optional | - | String getFrequency() | setFrequency(String frequency) |

## Example

```java
import com.verizon.thingspace.models.Configuration;

Configuration configuration = new Configuration.Builder()
    .frequency("Low")
    .build();
```


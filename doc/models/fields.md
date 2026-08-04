
# Fields

List of fields affected by the event.

## Structure

`Fields`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Configuration` | [`Configuration`](../../doc/models/configuration.md) | Optional | List of the field names and values to set. | Configuration getConfiguration() | setConfiguration(Configuration configuration) |

## Example

```java
import com.verizon.thingspace.models.Configuration;
import com.verizon.thingspace.models.Fields;

Fields fields = new Fields.Builder()
    .configuration(new Configuration.Builder()
        .frequency("Low")
        .build())
    .build();
```


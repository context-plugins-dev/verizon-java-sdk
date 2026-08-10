
# Connection Event

Network connection events for a device during a specified time period.

## Structure

`ConnectionEvent`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ConnectionEventAttributes` | [`List<CustomFields>`](../../doc/models/custom-fields.md) | Optional | The attributes that describe the connection event. | List<CustomFields> getConnectionEventAttributes() | setConnectionEventAttributes(List<CustomFields> connectionEventAttributes) |
| `ExtendedAttributes` | [`List<CustomFields>`](../../doc/models/custom-fields.md) | Optional | Currently not used. | List<CustomFields> getExtendedAttributes() | setExtendedAttributes(List<CustomFields> extendedAttributes) |
| `OccurredAt` | `String` | Optional | The date and time when the connection event occured. | String getOccurredAt() | setOccurredAt(String occurredAt) |

## Example

```java
import com.verizon.thingspace.models.ConnectionEvent;
import com.verizon.thingspace.models.CustomFields;
import java.util.Arrays;

ConnectionEvent connectionEvent = new ConnectionEvent.Builder()
    .connectionEventAttributes(Arrays.asList(
        new CustomFields.Builder(
            "BytesUsed"
        )
        .value("0")
        .build(),
        new CustomFields.Builder(
            "Event"
        )
        .value("Start")
        .build()
    ))
    .extendedAttributes(Arrays.asList(

    ))
    .occurredAt("2015-12-17T14:12:36-05:00")
    .build();
```


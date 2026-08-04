
# Key Data Percentage 50

## Structure

`KeyDataPercentage50`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Optional | - | String getKey() | setKey(String key) |
| `Value` | `Boolean` | Optional | - | Boolean getValue() | setValue(Boolean value) |

## Example

```java
import com.verizon.thingspace.models.KeyDataPercentage50;

KeyDataPercentage50 keyDataPercentage50 = new KeyDataPercentage50.Builder()
    .key("DataPercentage50")
    .value(false)
    .build();
```


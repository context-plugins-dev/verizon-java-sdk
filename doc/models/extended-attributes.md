
# Extended Attributes

Additional properties associated with data.

## Structure

`ExtendedAttributes`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Optional | - | String getKey() | setKey(String key) |
| `Value` | `String` | Optional | - | String getValue() | setValue(String value) |

## Example

```java
import com.verizon.thingspace.models.ExtendedAttributes;

ExtendedAttributes extendedAttributes = new ExtendedAttributes.Builder()
    .key("key8")
    .value("value0")
    .build();
```


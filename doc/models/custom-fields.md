
# Custom Fields

Custom data that can be included using key-value pairs.

## Structure

`CustomFields`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Required | The key for an extended attribute. | String getKey() | setKey(String key) |
| `Value` | `String` | Optional | The value of an extended attribute. | String getValue() | setValue(String value) |

## Example

```java
import com.verizon.thingspace.models.CustomFields;

CustomFields customFields = new CustomFields.Builder(
    "CustomField2"
)
.value("SuperVend")
.build();
```


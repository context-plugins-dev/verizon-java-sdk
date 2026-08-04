
# M5 G Bikey Value 1

## Structure

`M5gBikeyValue1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Optional | - | String getKey() | setKey(String key) |
| `Value` | `String` | Optional | - | String getValue() | setValue(String value) |

## Example

```java
import com.verizon.thingspace.models.M5gBikeyValue1;

M5gBikeyValue1 m5gBikeyValue1 = new M5gBikeyValue1.Builder()
    .key("CustomField1")
    .value("CF271")
    .build();
```


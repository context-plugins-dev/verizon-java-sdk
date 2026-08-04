
# M5 G Biattribute 2

## Structure

`M5gBiattribute2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Optional | - | String getKey() | setKey(String key) |
| `Value` | `String` | Optional | - | String getValue() | setValue(String value) |

## Example

```java
import com.verizon.thingspace.models.M5gBiattribute2;

M5gBiattribute2 m5gBiattribute2 = new M5gBiattribute2.Builder()
    .key("PrimaryPlaceOfUseFirstName")
    .value("string")
    .build();
```


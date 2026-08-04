
# Kv Pair

## Structure

`KvPair`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Optional | - | String getKey() | setKey(String key) |
| `Value` | `String` | Optional | - | String getValue() | setValue(String value) |

## Example

```java
import com.verizon.thingspace.models.KvPair;

KvPair kvPair = new KvPair.Builder()
    .key("key0")
    .value("value2")
    .build();
```



# Hpl Custom Fields

User assigned custom fields to use for fitering

## Structure

`HplCustomFields`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Optional | key property<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32` | String getKey() | setKey(String key) |
| `Value` | `String` | Optional | value of the key property<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `32` | String getValue() | setValue(String value) |

## Example

```java
import com.verizon.thingspace.models.HplCustomFields;

HplCustomFields hplCustomFields = new HplCustomFields.Builder()
    .key("key2")
    .value("value4")
    .build();
```


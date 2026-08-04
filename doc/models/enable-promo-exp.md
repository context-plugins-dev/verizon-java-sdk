
# Enable Promo Exp

## Structure

`EnablePromoExp`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Key` | `String` | Optional | - | String getKey() | setKey(String key) |
| `Value` | `Boolean` | Optional | - | Boolean getValue() | setValue(Boolean value) |

## Example

```java
import com.verizon.thingspace.models.EnablePromoExp;

EnablePromoExp enablePromoExp = new EnablePromoExp.Builder()
    .key("EnablePromoExp")
    .value(true)
    .build();
```


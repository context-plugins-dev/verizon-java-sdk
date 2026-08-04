
# Drop Response Item

## Structure

`DropResponseItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Imei` | `String` | Optional | - | String getImei() | setImei(String imei) |

## Example

```java
import com.verizon.thingspace.models.DropResponseItem;

DropResponseItem dropResponseItem = new DropResponseItem.Builder()
    .imei("100096454851324")
    .build();
```


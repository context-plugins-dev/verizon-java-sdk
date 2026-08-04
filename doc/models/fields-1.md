
# Fields 1

## Structure

`Fields1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Item` | [`SearchDeviceByPropertyFields`](../../doc/models/search-device-by-property-fields.md) | Optional | List of device sensors and their most recently reported values. | SearchDeviceByPropertyFields getItem() | setItem(SearchDeviceByPropertyFields item) |

## Example

```java
import com.verizon.thingspace.models.Acceleration;
import com.verizon.thingspace.models.Fields1;
import com.verizon.thingspace.models.SearchDeviceByPropertyFields;

Fields1 fields1 = new Fields1.Builder()
    .item(new SearchDeviceByPropertyFields.Builder()
        .acceleration(new Acceleration.Builder()
            .x("x6")
            .y("y4")
            .z("z6")
            .build())
        .battery("battery0")
        .humidity("humidity4")
        .light("light6")
        .pressure("pressure2")
        .build())
    .build();
```


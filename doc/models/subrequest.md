
# Subrequest

## Structure

`Subrequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ids` | [`GIODeviceId`](../../doc/models/gio-device-id.md) | Optional | - | GIODeviceId getIds() | setIds(GIODeviceId ids) |
| `Status` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `8`, *Pattern*: `^[A-Za-z]{3,8}$` | String getStatus() | setStatus(String status) |

## Example

```java
import com.verizon.thingspace.models.GIODeviceId;
import com.verizon.thingspace.models.Subrequest;

Subrequest subrequest = new Subrequest.Builder()
    .ids(new GIODeviceId.Builder(
        "kind2",
        "id4"
    )
    .build())
    .status("Success")
    .build();
```


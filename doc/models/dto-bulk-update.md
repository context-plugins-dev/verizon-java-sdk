
# Dto Bulk Update

## Structure

`DtoBulkUpdate`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Resourceidentifiers` | [`List<TheIDresourceandDeviceID>`](../../doc/models/the-i-dresourceand-device-id.md) | Optional | - | List<TheIDresourceandDeviceID> getResourceidentifiers() | setResourceidentifiers(List<TheIDresourceandDeviceID> resourceidentifiers) |
| `Smartalert` | [`BulkUpdateSmartalert`](../../doc/models/bulk-update-smartalert.md) | Optional | - | BulkUpdateSmartalert getSmartalert() | setSmartalert(BulkUpdateSmartalert smartalert) |

## Example

```java
import com.verizon.thingspace.models.BulkUpdateSmartalert;
import com.verizon.thingspace.models.DtoBulkUpdate;
import com.verizon.thingspace.models.TheIDresourceandDeviceID;
import java.util.Arrays;

DtoBulkUpdate dtoBulkUpdate = new DtoBulkUpdate.Builder()
    .accountname("0000123456-00001")
    .resourceidentifiers(Arrays.asList(
        new TheIDresourceandDeviceID.Builder()
            .id("ee70a869-eeee-ffff-gggg-07c14c31f96e")
            .deviceid("deviceid4")
            .build(),
        new TheIDresourceandDeviceID.Builder()
            .id("id4")
            .deviceid("131501ff-eeee-ffff-gggg-647d19179a12")
            .build()
    ))
    .smartalert(new BulkUpdateSmartalert.Builder()
        .name("name0")
        .build())
    .build();
```


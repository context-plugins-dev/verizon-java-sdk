
# Search Device by Property Response List

A success response includes an array of all matching devices.

## Structure

`SearchDeviceByPropertyResponseList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceProperty` | [`List<SearchDeviceByPropertyResponse>`](../../doc/models/search-device-by-property-response.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<SearchDeviceByPropertyResponse> getDeviceProperty() | setDeviceProperty(List<SearchDeviceByPropertyResponse> deviceProperty) |

## Example

```java
import com.verizon.thingspace.models.Acceleration;
import com.verizon.thingspace.models.Fields1;
import com.verizon.thingspace.models.SearchDeviceByPropertyFields;
import com.verizon.thingspace.models.SearchDeviceByPropertyResponse;
import com.verizon.thingspace.models.SearchDeviceByPropertyResponseList;
import java.util.Arrays;

SearchDeviceByPropertyResponseList searchDeviceByPropertyResponseList = new SearchDeviceByPropertyResponseList.Builder()
    .deviceProperty(Arrays.asList(
        new SearchDeviceByPropertyResponse.Builder()
            .billingaccountid("billingaccountid4")
            .createdon("createdon6")
            .eventretention("eventretention2")
            .fields(new Fields1.Builder()
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
                .build())
            .iccid("iccid4")
            .build(),
        new SearchDeviceByPropertyResponse.Builder()
            .billingaccountid("billingaccountid4")
            .createdon("createdon6")
            .eventretention("eventretention2")
            .fields(new Fields1.Builder()
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
                .build())
            .iccid("iccid4")
            .build(),
        new SearchDeviceByPropertyResponse.Builder()
            .billingaccountid("billingaccountid4")
            .createdon("createdon6")
            .eventretention("eventretention2")
            .fields(new Fields1.Builder()
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
                .build())
            .iccid("iccid4")
            .build()
    ))
    .build();
```


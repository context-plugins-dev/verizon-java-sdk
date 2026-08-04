
# Find Device by Property Response List

A success response includes an array of all matching devices. Each device includes the full device resource definition.

## Structure

`FindDeviceByPropertyResponseList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceProperty` | [`List<FindDeviceByPropertyResponse>`](../../doc/models/find-device-by-property-response.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<FindDeviceByPropertyResponse> getDeviceProperty() | setDeviceProperty(List<FindDeviceByPropertyResponse> deviceProperty) |

## Example

```java
import com.verizon.thingspace.models.FindDeviceByPropertyResponse;
import com.verizon.thingspace.models.FindDeviceByPropertyResponseList;
import java.util.Arrays;

FindDeviceByPropertyResponseList findDeviceByPropertyResponseList = new FindDeviceByPropertyResponseList.Builder()
    .deviceProperty(Arrays.asList(
        new FindDeviceByPropertyResponse.Builder()
            .billingaccountid("billingaccountid4")
            .createdon("createdon6")
            .eventretention("eventretention2")
            .iccid("iccid4")
            .id("id8")
            .build(),
        new FindDeviceByPropertyResponse.Builder()
            .billingaccountid("billingaccountid4")
            .createdon("createdon6")
            .eventretention("eventretention2")
            .iccid("iccid4")
            .id("id8")
            .build(),
        new FindDeviceByPropertyResponse.Builder()
            .billingaccountid("billingaccountid4")
            .createdon("createdon6")
            .eventretention("eventretention2")
            .iccid("iccid4")
            .id("id8")
            .build()
    ))
    .build();
```


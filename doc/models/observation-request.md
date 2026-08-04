
# Observation Request

Used to define callbacks including the device identity, the attribute names, corresponding attribute values and the date/timestamp of when the observation was made.

## Structure

`ObservationRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account identifier in "##########-#####". | String getAccountName() | setAccountName(String accountName) |
| `Devices` | [`List<Device>`](../../doc/models/device.md) | Required | List of devices. | List<Device> getDevices() | setDevices(List<Device> devices) |
| `Attributes` | [`List<ObservationRequestAttribute>`](../../doc/models/observation-request-attribute.md) | Required | Attributes are streaming RF parameters that you want to observe. | List<ObservationRequestAttribute> getAttributes() | setAttributes(List<ObservationRequestAttribute> attributes) |
| `Frequency` | [`NumericalData`](../../doc/models/numerical-data.md) | Optional | Describes value and unit of time. | NumericalData getFrequency() | setFrequency(NumericalData frequency) |
| `Duration` | [`NumericalData`](../../doc/models/numerical-data.md) | Optional | Describes value and unit of time. | NumericalData getDuration() | setDuration(NumericalData duration) |

## Example

```java
import com.verizon.thingspace.models.AttributeIdentifierEnum;
import com.verizon.thingspace.models.Device;
import com.verizon.thingspace.models.ObservationRequest;
import com.verizon.thingspace.models.ObservationRequestAttribute;
import java.util.Arrays;

ObservationRequest observationRequest = new ObservationRequest.Builder(
    "0000123456-00001",
    Arrays.asList(
        new Device.Builder(
            "864508030026238",
            "IMEI"
        )
        .build()
    ),
    Arrays.asList(
        new ObservationRequestAttribute.Builder()
            .name(AttributeIdentifierEnum.RADIO_SIGNAL_STRENGTH)
            .build(),
        new ObservationRequestAttribute.Builder()
            .name(AttributeIdentifierEnum.LINK_QUALITY)
            .build(),
        new ObservationRequestAttribute.Builder()
            .name(AttributeIdentifierEnum.NETWORK_BEARER)
            .build(),
        new ObservationRequestAttribute.Builder()
            .name(AttributeIdentifierEnum.CELL_ID)
            .build()
    )
)
.frequency(null)
.duration(null)
.build();
```


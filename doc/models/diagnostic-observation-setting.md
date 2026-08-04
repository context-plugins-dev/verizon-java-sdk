
# Diagnostic Observation Setting

Diagnostic observation settings and attributes for a device.

## Structure

`DiagnosticObservationSetting`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | The name of the billing account for which callback messages will be sent. Format: "##########-#####". | String getAccountName() | setAccountName(String accountName) |
| `Device` | [`Device`](../../doc/models/device.md) | Optional | Identifies a particular IoT device. | Device getDevice() | setDevice(Device device) |
| `Attributes` | [`List<AttributeSetting>`](../../doc/models/attribute-setting.md) | Optional | Streaming RF parameters for which you want to retrieve diagnostic settings. | List<AttributeSetting> getAttributes() | setAttributes(List<AttributeSetting> attributes) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.AttributeIdentifierEnum;
import com.verizon.thingspace.models.AttributeSetting;
import com.verizon.thingspace.models.Device;
import com.verizon.thingspace.models.DiagnosticObservationSetting;
import com.verizon.thingspace.models.NumericalData;
import com.verizon.thingspace.models.NumericalDataUnitEnum;
import java.util.Arrays;

DiagnosticObservationSetting diagnosticObservationSetting = new DiagnosticObservationSetting.Builder()
    .accountName("string")
    .device(new Device.Builder(
        "864508030026238",
        "IMEI"
    )
    .build())
    .attributes(Arrays.asList(
        new AttributeSetting.Builder()
            .name(AttributeIdentifierEnum.MANUFACTURER)
            .value("string")
            .createdOn(DateTimeHelper.fromRfc8601DateTime("2019-09-07T23:08:03.532Z"))
            .isObservable(true)
            .isObserving(true)
            .frequency(new NumericalData.Builder()
                .value(5)
                .unit(NumericalDataUnitEnum.SECOND)
                .build())
            .build()
    ))
    .build();
```


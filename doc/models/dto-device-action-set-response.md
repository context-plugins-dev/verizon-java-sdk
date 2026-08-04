
# Dto Device Action Set Response

## Structure

`DtoDeviceActionSetResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Actionresult` | [`List<ActionResultwithDeviceConfig>`](../../doc/models/action-resultwith-device-config.md) | Optional | - | List<ActionResultwithDeviceConfig> getActionresult() | setActionresult(List<ActionResultwithDeviceConfig> actionresult) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.ActionResultwithDeviceConfig;
import com.verizon.thingspace.models.DtoDeviceActionSetConfiguration;
import com.verizon.thingspace.models.DtoDeviceActionSetResponse;
import com.verizon.thingspace.models.DtoDeviceConfig;
import com.verizon.thingspace.models.SensorInsightsBLE;
import java.util.Arrays;

DtoDeviceActionSetResponse dtoDeviceActionSetResponse = new DtoDeviceActionSetResponse.Builder()
    .actionresult(Arrays.asList(
        new ActionResultwithDeviceConfig.Builder()
            .createdon(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .description("description8")
            .deviceid("deviceid8")
            .errmsg("errmsg0")
            .fields(new DtoDeviceActionSetConfiguration.Builder()
                .deviceConfig(new DtoDeviceConfig.Builder()
                    .ble(new SensorInsightsBLE.Builder()
                        .dataMode(216)
                        .manufacturerId(180)
                        .maxNumScan(126)
                        .minSigStr(60)
                        .monitorPeriod(88)
                        .build())
                    .build())
                .build())
            .build(),
        new ActionResultwithDeviceConfig.Builder()
            .createdon(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .description("description8")
            .deviceid("deviceid8")
            .errmsg("errmsg0")
            .fields(new DtoDeviceActionSetConfiguration.Builder()
                .deviceConfig(new DtoDeviceConfig.Builder()
                    .ble(new SensorInsightsBLE.Builder()
                        .dataMode(216)
                        .manufacturerId(180)
                        .maxNumScan(126)
                        .minSigStr(60)
                        .monitorPeriod(88)
                        .build())
                    .build())
                .build())
            .build(),
        new ActionResultwithDeviceConfig.Builder()
            .createdon(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .description("description8")
            .deviceid("deviceid8")
            .errmsg("errmsg0")
            .fields(new DtoDeviceActionSetConfiguration.Builder()
                .deviceConfig(new DtoDeviceConfig.Builder()
                    .ble(new SensorInsightsBLE.Builder()
                        .dataMode(216)
                        .manufacturerId(180)
                        .maxNumScan(126)
                        .minSigStr(60)
                        .monitorPeriod(88)
                        .build())
                    .build())
                .build())
            .build()
    ))
    .build();
```


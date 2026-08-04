
# Dto Device Config

## Structure

`DtoDeviceConfig`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ble` | [`SensorInsightsBLE`](../../doc/models/sensor-insights-ble.md) | Optional | Property objects for Bluetooth Low-Energy (BLE) devices | SensorInsightsBLE getBle() | setBle(SensorInsightsBLE ble) |

## Example

```java
import com.verizon.thingspace.models.DtoDeviceConfig;
import com.verizon.thingspace.models.SensorInsightsBLE;

DtoDeviceConfig dtoDeviceConfig = new DtoDeviceConfig.Builder()
    .ble(new SensorInsightsBLE.Builder()
        .dataMode(216)
        .manufacturerId(180)
        .maxNumScan(126)
        .minSigStr(60)
        .monitorPeriod(88)
        .build())
    .build();
```


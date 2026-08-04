
# Sensorinsightsconfig

The configuration of the remove request

## Structure

`Sensorinsightsconfig`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Removesensor` | [`DtoOffBoardSensor`](../../doc/models/dto-off-board-sensor.md) | Optional | The EUI64 address of the device being removed | DtoOffBoardSensor getRemovesensor() | setRemovesensor(DtoOffBoardSensor removesensor) |

## Example

```java
import com.verizon.thingspace.models.DtoOffBoardSensor;
import com.verizon.thingspace.models.Sensorinsightsconfig;

Sensorinsightsconfig sensorinsightsconfig = new Sensorinsightsconfig.Builder()
    .removesensor(new DtoOffBoardSensor.Builder()
        .deveui("deveui6")
        .build())
    .build();
```


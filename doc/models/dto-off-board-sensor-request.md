
# Dto Off Board Sensor Request

## Structure

`DtoOffBoardSensorRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Configuration` | [`Sensorinsightsconfig`](../../doc/models/sensorinsightsconfig.md) | Optional | The configuration of the remove request | Sensorinsightsconfig getConfiguration() | setConfiguration(Sensorinsightsconfig configuration) |

## Example

```java
import com.verizon.thingspace.models.DtoOffBoardSensor;
import com.verizon.thingspace.models.DtoOffBoardSensorRequest;
import com.verizon.thingspace.models.Sensorinsightsconfig;

DtoOffBoardSensorRequest dtoOffBoardSensorRequest = new DtoOffBoardSensorRequest.Builder()
    .accountname("0000123456-00001")
    .configuration(new Sensorinsightsconfig.Builder()
        .removesensor(new DtoOffBoardSensor.Builder()
            .deveui("deveui6")
            .build())
        .build())
    .build();
```


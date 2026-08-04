
# Dto Sensor Off Boarding Status Response

## Structure

`DtoSensorOffBoardingStatusResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Events` | [`List<DtoSensorBoardingEvent>`](../../doc/models/dto-sensor-boarding-event.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<DtoSensorBoardingEvent> getEvents() | setEvents(List<DtoSensorBoardingEvent> events) |
| `Isstillregistered` | `Boolean` | Optional | - | Boolean getIsstillregistered() | setIsstillregistered(Boolean isstillregistered) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DtoSensorBoardingEvent;
import com.verizon.thingspace.models.DtoSensorOffBoardingStatusResponse;
import java.util.Arrays;

DtoSensorOffBoardingStatusResponse dtoSensorOffBoardingStatusResponse = new DtoSensorOffBoardingStatusResponse.Builder()
    .events(Arrays.asList(
        new DtoSensorBoardingEvent.Builder()
            .createdon(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errmsg("errmsg2")
            .fields(null)
            .state("state6")
            .transactionid("transactionid8")
            .build(),
        new DtoSensorBoardingEvent.Builder()
            .createdon(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errmsg("errmsg2")
            .fields(null)
            .state("state6")
            .transactionid("transactionid8")
            .build()
    ))
    .isstillregistered(true)
    .build();
```


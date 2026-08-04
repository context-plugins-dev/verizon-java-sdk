
# Dto Sensor on Boarding Status Response

## Structure

`DtoSensorOnBoardingStatusResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Events` | [`List<DtoSensorBoardingEvent>`](../../doc/models/dto-sensor-boarding-event.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<DtoSensorBoardingEvent> getEvents() | setEvents(List<DtoSensorBoardingEvent> events) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DtoSensorBoardingEvent;
import com.verizon.thingspace.models.DtoSensorOnBoardingStatusResponse;
import java.util.Arrays;

DtoSensorOnBoardingStatusResponse dtoSensorOnBoardingStatusResponse = new DtoSensorOnBoardingStatusResponse.Builder()
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
            .build(),
        new DtoSensorBoardingEvent.Builder()
            .createdon(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errmsg("errmsg2")
            .fields(null)
            .state("state6")
            .transactionid("transactionid8")
            .build()
    ))
    .build();
```


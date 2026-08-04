
# Dto Health Score Summary

The values measured are for sensors and gateways

## Structure

`DtoHealthScoreSummary`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Overallsummary` | [`List<DtoHealthScoreMetric>`](../../doc/models/dto-health-score-metric.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<DtoHealthScoreMetric> getOverallsummary() | setOverallsummary(List<DtoHealthScoreMetric> overallsummary) |

## Example

```java
import com.verizon.thingspace.models.DtoHealthScoreMetric;
import com.verizon.thingspace.models.DtoHealthScoreSummary;
import java.util.Arrays;

DtoHealthScoreSummary dtoHealthScoreSummary = new DtoHealthScoreSummary.Builder()
    .overallsummary(Arrays.asList(
        new DtoHealthScoreMetric.Builder()
            .metrictype("metrictype0")
            .metricvalue("metricvalue6")
            .build(),
        new DtoHealthScoreMetric.Builder()
            .metrictype("metrictype0")
            .metricvalue("metricvalue6")
            .build()
    ))
    .build();
```


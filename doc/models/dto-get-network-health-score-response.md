
# Dto Get Network Health Score Response

The values measured are for the network

## Structure

`DtoGetNetworkHealthScoreResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Networksummary` | [`List<DtoHealthScoreMetric>`](../../doc/models/dto-health-score-metric.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<DtoHealthScoreMetric> getNetworksummary() | setNetworksummary(List<DtoHealthScoreMetric> networksummary) |
| `Overallsummary` | [`List<DtoHealthScoreMetric>`](../../doc/models/dto-health-score-metric.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<DtoHealthScoreMetric> getOverallsummary() | setOverallsummary(List<DtoHealthScoreMetric> overallsummary) |

## Example

```java
import com.verizon.thingspace.models.DtoGetNetworkHealthScoreResponse;
import com.verizon.thingspace.models.DtoHealthScoreMetric;
import java.util.Arrays;

DtoGetNetworkHealthScoreResponse dtoGetNetworkHealthScoreResponse = new DtoGetNetworkHealthScoreResponse.Builder()
    .networksummary(Arrays.asList(
        new DtoHealthScoreMetric.Builder()
            .metrictype("networkscore")
            .metricvalue("95")
            .build()
    ))
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



# Dto Query Metrics

## Structure

`DtoQueryMetrics`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Days` | `Integer` | Optional | The number of days in a recent period to query | Integer getDays() | setDays(Integer days) |

## Example

```java
import com.verizon.thingspace.models.DtoQueryMetrics;

DtoQueryMetrics dtoQueryMetrics = new DtoQueryMetrics.Builder()
    .days(30)
    .build();
```


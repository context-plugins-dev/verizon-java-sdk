
# Filtercriteria 2

## Structure

`Filtercriteria2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FilterCriteria` | `List<Object>` | Optional | - | List<Object> getFilterCriteria() | setFilterCriteria(List<Object> filterCriteria) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.Filtercriteria2;
import java.io.IOException;
import java.util.Arrays;

Filtercriteria2 filtercriteria2 = new Filtercriteria2.Builder()
    .filterCriteria(Arrays.asList(
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
    ))
    .build();
```


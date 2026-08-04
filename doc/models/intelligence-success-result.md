
# Intelligence Success Result

Success response.

## Structure

`IntelligenceSuccessResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Status` | `String` | Optional | Anomaly detection status. | String getStatus() | setStatus(String status) |

## Example

```java
import com.verizon.thingspace.models.IntelligenceSuccessResult;

IntelligenceSuccessResult intelligenceSuccessResult = new IntelligenceSuccessResult.Builder()
    .status("Success")
    .build();
```


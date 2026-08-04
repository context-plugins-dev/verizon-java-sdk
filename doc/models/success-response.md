
# Success Response

## Structure

`SuccessResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Success` | `Boolean` | Optional | - | Boolean getSuccess() | setSuccess(Boolean success) |

## Example

```java
import com.verizon.thingspace.models.SuccessResponse;

SuccessResponse successResponse = new SuccessResponse.Builder()
    .success(true)
    .build();
```


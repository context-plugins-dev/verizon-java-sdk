
# Api Response Code

ResponseCode and/or a message indicating success or failure of the request.

## Structure

`ApiResponseCode`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResponseCode` | [`ResponseCodeEnum`](../../doc/models/response-code-enum.md) | Required | Possible response codes. | ResponseCodeEnum getResponseCode() | setResponseCode(ResponseCodeEnum responseCode) |
| `Message` | `String` | Required | More details about the responseCode received. | String getMessage() | setMessage(String message) |

## Example

```java
import com.verizon.thingspace.models.ApiResponseCode;
import com.verizon.thingspace.models.ResponseCodeEnum;

ApiResponseCode apiResponseCode = new ApiResponseCode.Builder(
    ResponseCodeEnum.INVALID_ACCESS,
    "message2"
)
.build();
```


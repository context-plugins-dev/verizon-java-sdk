
# Aggregate Usage Error

Error reported by a device.

## Structure

`AggregateUsageError`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Imei` | `String` | Optional | The International Mobile Equipment Identifier of the device. | String getImei() | setImei(String imei) |
| `ErrorMessage` | `String` | Optional | A general error message. | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `ErrorResponse` | [`IErrorMessage`](../../doc/models/i-error-message.md) | Optional | Error message. | IErrorMessage getErrorResponse() | setErrorResponse(IErrorMessage errorResponse) |

## Example

```java
import com.verizon.thingspace.models.AggregateUsageError;
import com.verizon.thingspace.models.ErrorResponseCodeEnum;
import com.verizon.thingspace.models.HttpStatusCodeEnum;
import com.verizon.thingspace.models.IErrorMessage;

AggregateUsageError aggregateUsageError = new AggregateUsageError.Builder()
    .imei("15-digit IMEI")
    .errorMessage("errorMessage8")
    .errorResponse(new IErrorMessage.Builder()
        .errorCode(ErrorResponseCodeEnum.INVALID_PARAMETER)
        .errorMessage("errorMessage4")
        .httpStatusCode(HttpStatusCodeEnum.ENUM_423_LOCKED)
        .detailErrorMessage("detailErrorMessage6")
        .build())
    .build();
```


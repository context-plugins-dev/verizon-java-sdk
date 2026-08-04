
# Aggregate Session Report

Session and usage details for up to 10 devices.

## Structure

`AggregateSessionReport`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Txid` | `String` | Optional | A unique string (UUID) that associates the request with the location report information that is sent in asynchronous callback message.ThingSpace will send a separate callback message for each device that was in the request. All of the callback messages will have a txid. | String getTxid() | setTxid(String txid) |
| `Usage` | [`List<AggregateUsageItem>`](../../doc/models/aggregate-usage-item.md) | Optional | Contains usage per device.<br><br>**Constraints**: *Unique Items Required* | List<AggregateUsageItem> getUsage() | setUsage(List<AggregateUsageItem> usage) |
| `Errors` | [`List<AggregateUsageError>`](../../doc/models/aggregate-usage-error.md) | Optional | An object containing any errors reported by the device.<br><br>**Constraints**: *Unique Items Required* | List<AggregateUsageError> getErrors() | setErrors(List<AggregateUsageError> errors) |

## Example

```java
import com.verizon.thingspace.models.AggregateSessionReport;
import com.verizon.thingspace.models.AggregateUsageError;
import com.verizon.thingspace.models.AggregateUsageItem;
import com.verizon.thingspace.models.ErrorResponseCodeEnum;
import com.verizon.thingspace.models.HttpStatusCodeEnum;
import com.verizon.thingspace.models.IErrorMessage;
import java.util.Arrays;

AggregateSessionReport aggregateSessionReport = new AggregateSessionReport.Builder()
    .txid("60c07fff-eeee-ffff-gggg-75e6a7c238f6")
    .usage(Arrays.asList(
        new AggregateUsageItem.Builder()
            .imei("15-digit IMEI")
            .numberOfSessions(1)
            .bytesTransferred(2057)
            .build()
    ))
    .errors(Arrays.asList(
        new AggregateUsageError.Builder()
            .imei("imei6")
            .errorMessage("errorMessage8")
            .errorResponse(new IErrorMessage.Builder()
                .errorCode(ErrorResponseCodeEnum.INVALID_PARAMETER)
                .errorMessage("errorMessage4")
                .httpStatusCode(HttpStatusCodeEnum.ENUM_423_LOCKED)
                .detailErrorMessage("detailErrorMessage6")
                .build())
            .build(),
        new AggregateUsageError.Builder()
            .imei("imei6")
            .errorMessage("errorMessage8")
            .errorResponse(new IErrorMessage.Builder()
                .errorCode(ErrorResponseCodeEnum.INVALID_PARAMETER)
                .errorMessage("errorMessage4")
                .httpStatusCode(HttpStatusCodeEnum.ENUM_423_LOCKED)
                .detailErrorMessage("detailErrorMessage6")
                .build())
            .build(),
        new AggregateUsageError.Builder()
            .imei("imei6")
            .errorMessage("errorMessage8")
            .errorResponse(new IErrorMessage.Builder()
                .errorCode(ErrorResponseCodeEnum.INVALID_PARAMETER)
                .errorMessage("errorMessage4")
                .httpStatusCode(HttpStatusCodeEnum.ENUM_423_LOCKED)
                .detailErrorMessage("detailErrorMessage6")
                .build())
            .build()
    ))
    .build();
```



# Fota V2 Success Result

Response to a successful request.

## Structure

`FotaV2SuccessResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Success` | `boolean` | Required | - | boolean getSuccess() | setSuccess(boolean success) |

## Example

```java
import com.verizon.thingspace.models.FotaV2SuccessResult;

FotaV2SuccessResult fotaV2SuccessResult = new FotaV2SuccessResult.Builder(
    true
)
.build();
```



# Fota V3 Success Result

Cancelation status.

## Structure

`FotaV3SuccessResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Success` | `boolean` | Required | True or false. | boolean getSuccess() | setSuccess(boolean success) |

## Example

```java
import com.verizon.thingspace.models.FotaV3SuccessResult;

FotaV3SuccessResult fotaV3SuccessResult = new FotaV3SuccessResult.Builder(
    true
)
.build();
```


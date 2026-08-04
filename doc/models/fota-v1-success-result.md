
# Fota V1 Success Result

A response to a successful request contains a single Boolean value.

## Structure

`FotaV1SuccessResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Success` | `Boolean` | Optional | True is returned in case of success. | Boolean getSuccess() | setSuccess(Boolean success) |

## Example

```java
import com.verizon.thingspace.models.FotaV1SuccessResult;

FotaV1SuccessResult fotaV1SuccessResult = new FotaV1SuccessResult.Builder()
    .success(true)
    .build();
```


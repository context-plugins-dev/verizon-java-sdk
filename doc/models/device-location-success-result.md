
# Device Location Success Result

Whether the device location request was successful or not.

## Structure

`DeviceLocationSuccessResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Success` | `Boolean` | Optional | - | Boolean getSuccess() | setSuccess(Boolean success) |

## Example

```java
import com.verizon.thingspace.models.DeviceLocationSuccessResult;

DeviceLocationSuccessResult deviceLocationSuccessResult = new DeviceLocationSuccessResult.Builder()
    .success(true)
    .build();
```


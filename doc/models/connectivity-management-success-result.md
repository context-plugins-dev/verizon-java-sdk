
# Connectivity Management Success Result

Response to successful request.

## Structure

`ConnectivityManagementSuccessResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Success` | `Boolean` | Optional | A value of “true” indicates that the device group was created successfully. | Boolean getSuccess() | setSuccess(Boolean success) |

## Example

```java
import com.verizon.thingspace.models.ConnectivityManagementSuccessResult;

ConnectivityManagementSuccessResult connectivityManagementSuccessResult = new ConnectivityManagementSuccessResult.Builder()
    .success(true)
    .build();
```


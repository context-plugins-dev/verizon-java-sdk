
# Retrieve Response Item

## Structure

`RetrieveResponseItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Imei` | `String` | Optional | - | String getImei() | setImei(String imei) |
| `Username` | `String` | Optional | Present if credentials exist | String getUsername() | setUsername(String username) |
| `Failure` | `String` | Optional | Present if retrieval failed | String getFailure() | setFailure(String failure) |

## Example

```java
import com.verizon.thingspace.models.RetrieveResponseItem;

RetrieveResponseItem retrieveResponseItem = new RetrieveResponseItem.Builder()
    .imei("100096454851324")
    .username("290sk9vmybmxi1kmx1kxo8w13u")
    .failure("No active username")
    .build();
```


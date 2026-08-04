
# Callback Registered

Callback listener is Registered.

## Structure

`CallbackRegistered`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | The numeric name of the account and must include leading zeroes. | String getAccountName() | setAccountName(String accountName) |
| `Name` | `String` | Required | The name of the callback service, which identifies the type and format of messages that will be sent to the registered URL. | String getName() | setName(String name) |

## Example

```java
import com.verizon.thingspace.models.CallbackRegistered;

CallbackRegistered callbackRegistered = new CallbackRegistered.Builder(
    "0000123456-00001",
    "BullseyeReporting"
)
.build();
```


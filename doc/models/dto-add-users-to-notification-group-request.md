
# Dto Add Users to Notification Group Request

## Structure

`DtoAddUsersToNotificationGroupRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Id` | `String` | Optional | UUID of the user record, assigned at creation | String getId() | setId(String id) |
| `Userids` | `List<String>` | Optional | - | List<String> getUserids() | setUserids(List<String> userids) |

## Example

```java
import com.verizon.thingspace.models.DtoAddUsersToNotificationGroupRequest;
import java.util.Arrays;

DtoAddUsersToNotificationGroupRequest dtoAddUsersToNotificationGroupRequest = new DtoAddUsersToNotificationGroupRequest.Builder()
    .accountname("0000123456-00001")
    .id("id0")
    .userids(Arrays.asList(
        "userids8",
        "userids7",
        "userids6"
    ))
    .build();
```



# Dto Update Notification Group Request

## Structure

`DtoUpdateNotificationGroupRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Group` | [`DtoNotificationGroupRequestEntity`](../../doc/models/dto-notification-group-request-entity.md) | Required | - | DtoNotificationGroupRequestEntity getGroup() | setGroup(DtoNotificationGroupRequestEntity group) |
| `Id` | `String` | Optional | UUID of the user record, assigned at creation | String getId() | setId(String id) |
| `Userids` | `List<String>` | Optional | - | List<String> getUserids() | setUserids(List<String> userids) |

## Example

```java
import com.verizon.thingspace.models.DtoNotificationGroupRequestEntity;
import com.verizon.thingspace.models.DtoUpdateNotificationGroupRequest;
import java.util.Arrays;

DtoUpdateNotificationGroupRequest dtoUpdateNotificationGroupRequest = new DtoUpdateNotificationGroupRequest.Builder(
    new DtoNotificationGroupRequestEntity.Builder()
        .description("a short description")
        .groupemail("email@domain.com")
        .name("name of the record")
        .build()
)
.accountname("0000123456-00001")
.id("id4")
.userids(Arrays.asList(
        "userids8"
    ))
.build();
```


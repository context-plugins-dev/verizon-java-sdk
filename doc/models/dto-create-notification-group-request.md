
# Dto Create Notification Group Request

## Structure

`DtoCreateNotificationGroupRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Group` | [`DtoNotificationGroupRequestEntity`](../../doc/models/dto-notification-group-request-entity.md) | Required | - | DtoNotificationGroupRequestEntity getGroup() | setGroup(DtoNotificationGroupRequestEntity group) |
| `Userids` | `List<String>` | Optional | - | List<String> getUserids() | setUserids(List<String> userids) |

## Example

```java
import com.verizon.thingspace.models.DtoCreateNotificationGroupRequest;
import com.verizon.thingspace.models.DtoNotificationGroupRequestEntity;
import java.util.Arrays;

DtoCreateNotificationGroupRequest dtoCreateNotificationGroupRequest = new DtoCreateNotificationGroupRequest.Builder(
    new DtoNotificationGroupRequestEntity.Builder()
        .description("a short description")
        .groupemail("email@domain.com")
        .name("name of the record")
        .build()
)
.accountname("0000123456-00001")
.userids(Arrays.asList(
        "userids0"
    ))
.build();
```


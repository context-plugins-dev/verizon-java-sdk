
# Dto Update User Request

## Structure

`DtoUpdateUserRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Id` | `String` | Optional | UUID of the user record, assigned at creation | String getId() | setId(String id) |
| `User` | [`DtoUserDTO`](../../doc/models/dto-user-dto.md) | Optional | - | DtoUserDTO getUser() | setUser(DtoUserDTO user) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.DtoUpdateUserRequest;
import com.verizon.thingspace.models.DtoUserDTO;
import java.io.IOException;
import java.util.LinkedHashMap;

DtoUpdateUserRequest dtoUpdateUserRequest = new DtoUpdateUserRequest.Builder()
    .accountname("0000123456-00001")
    .id("id0")
    .user(new DtoUserDTO.Builder()
        .email("email6")
        .firstname("firstname8")
        .lastname("lastname6")
        .mdn("mdn8")
        .customdata(new LinkedHashMap<String, Object>() {{
            put("key0", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"));
            put("key1", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"));
            put("key2", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"));
        }})
        .build())
    .build();
```


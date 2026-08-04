
# Dto Create User Request

## Structure

`DtoCreateUserRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `User` | [`DtoUserDTO`](../../doc/models/dto-user-dto.md) | Optional | - | DtoUserDTO getUser() | setUser(DtoUserDTO user) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.DtoCreateUserRequest;
import com.verizon.thingspace.models.DtoUserDTO;
import java.io.IOException;
import java.util.LinkedHashMap;

DtoCreateUserRequest dtoCreateUserRequest = new DtoCreateUserRequest.Builder()
    .accountname("0000123456-00001")
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



# Dto Configuration Profile Path

## Structure

`DtoConfigurationProfilePath`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountName() | setAccountName(String accountName) |
| `Resourceidentifier` | [`DtoResourceidentifier`](../../doc/models/dto-resourceidentifier.md) | Optional | - | DtoResourceidentifier getResourceidentifier() | setResourceidentifier(DtoResourceidentifier resourceidentifier) |
| `Profile` | [`DtoProfile`](../../doc/models/dto-profile.md) | Optional | - | DtoProfile getProfile() | setProfile(DtoProfile profile) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.DtoConfigurationProfilePath;
import com.verizon.thingspace.models.DtoProfile;
import com.verizon.thingspace.models.DtoResourceidentifier;
import java.io.IOException;

DtoConfigurationProfilePath dtoConfigurationProfilePath = new DtoConfigurationProfilePath.Builder()
    .accountName("0000123456-00001")
    .resourceidentifier(new DtoResourceidentifier.Builder()
        .id("id4")
        .build())
    .profile(new DtoProfile.Builder()
        .kind("kind8")
        .version("version6")
        .modelid("modelid4")
        .name("name0")
        .configuration(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .build();
```


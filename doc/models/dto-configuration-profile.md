
# Dto Configuration Profile

## Structure

`DtoConfigurationProfile`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountname` | `String` | Optional | The numeric account name, which must include leading zeros | String getAccountname() | setAccountname(String accountname) |
| `Profiles` | [`List<DtoProfile>`](../../doc/models/dto-profile.md) | Optional | - | List<DtoProfile> getProfiles() | setProfiles(List<DtoProfile> profiles) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.DtoConfigurationProfile;
import com.verizon.thingspace.models.DtoProfile;
import java.io.IOException;
import java.util.Arrays;

DtoConfigurationProfile dtoConfigurationProfile = new DtoConfigurationProfile.Builder()
    .accountname("0000123456-00001")
    .profiles(Arrays.asList(
        new DtoProfile.Builder()
            .kind("kind6")
            .version("version4")
            .modelid("modelid2")
            .name("name8")
            .configuration(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .build();
```


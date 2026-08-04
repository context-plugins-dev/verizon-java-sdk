
# PWN Profile List

## Structure

`PWNProfileList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Profiles` | [`List<PWNProfile>`](../../doc/models/pwn-profile.md) | Optional | - | List<PWNProfile> getProfiles() | setProfiles(List<PWNProfile> profiles) |

## Example

```java
import com.verizon.thingspace.models.PWNProfile;
import com.verizon.thingspace.models.PWNProfileList;
import java.util.Arrays;

PWNProfileList pWNProfileList = new PWNProfileList.Builder()
    .profiles(Arrays.asList(
        new PWNProfile.Builder()
            .profileId("HSS-EsmProfile_Enterprise")
            .profileName("HSS EsmProfile Enterprise")
            .build()
    ))
    .build();
```



# PWN Profile

## Structure

`PWNProfile`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ProfileId` | `String` | Optional | - | String getProfileId() | setProfileId(String profileId) |
| `ProfileName` | `String` | Optional | - | String getProfileName() | setProfileName(String profileName) |

## Example

```java
import com.verizon.thingspace.models.PWNProfile;

PWNProfile pWNProfile = new PWNProfile.Builder()
    .profileId("HSS-EsmProfile_Enterprise")
    .profileName("HSS EsmProfile Enterprise")
    .build();
```



# Consent Request

## Structure

`ConsentRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account identifier in "##########-#####". | String getAccountName() | setAccountName(String accountName) |
| `AllDevice` | `Boolean` | Optional | Exclude all devices or not. | Boolean getAllDevice() | setAllDevice(Boolean allDevice) |
| `Type` | `String` | Optional | The change to make: append or replace. | String getType() | setType(String type) |
| `Exclusion` | `List<String>` | Optional | Device ID list. | List<String> getExclusion() | setExclusion(List<String> exclusion) |

## Example

```java
import com.verizon.thingspace.models.ConsentRequest;
import java.util.Arrays;

ConsentRequest consentRequest = new ConsentRequest.Builder(
    "1234567890-00001"
)
.allDevice(false)
.type("replace")
.exclusion(Arrays.asList(
        "980003420535573",
        "375535024300089",
        "A100003861E585"
    ))
.build();
```


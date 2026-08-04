
# Device Credential Request Item

## Structure

`DeviceCredentialRequestItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Imei` | `String` | Required | 15-digit alphanumeric identifier<br><br>**Constraints**: *Pattern*: `^[A-Za-z0-9]{15}$` | String getImei() | setImei(String imei) |

## Example

```java
import com.verizon.thingspace.models.DeviceCredentialRequestItem;

DeviceCredentialRequestItem deviceCredentialRequestItem = new DeviceCredentialRequestItem.Builder(
    "221000008775573"
)
.build();
```


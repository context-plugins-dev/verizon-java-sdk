
# Private Network Apns

## Structure

`PrivateNetworkApns`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ApnName` | `String` | Optional | the Access Point Name | String getApnName() | setApnName(String apnName) |
| `AddressAssignmentMethod` | `String` | Optional | The method used for address assignment. | String getAddressAssignmentMethod() | setAddressAssignmentMethod(String addressAssignmentMethod) |
| `Ipaddress` | `String` | Optional | A IPv4 address | String getIpaddress() | setIpaddress(String ipaddress) |

## Example

```java
import com.verizon.thingspace.models.PrivateNetworkApns;

PrivateNetworkApns privateNetworkApns = new PrivateNetworkApns.Builder()
    .apnName("apnName2")
    .addressAssignmentMethod("addressAssignmentMethod8")
    .ipaddress("10.10.10.01")
    .build();
```


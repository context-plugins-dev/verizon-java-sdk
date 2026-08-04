
# V1 Licenses Assigned Removed Request

IMEIs of the devices to assign licenses to.

## Structure

`V1LicensesAssignedRemovedRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceList` | `List<String>` | Required | The IMEIs of the devices. | List<String> getDeviceList() | setDeviceList(List<String> deviceList) |

## Example

```java
import com.verizon.thingspace.models.V1LicensesAssignedRemovedRequest;
import java.util.Arrays;

V1LicensesAssignedRemovedRequest v1LicensesAssignedRemovedRequest = new V1LicensesAssignedRemovedRequest.Builder(
    Arrays.asList(
        "900000000000001",
        "900000000000998",
        "900000000000999"
    )
)
.build();
```


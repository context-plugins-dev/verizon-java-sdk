
# Account Device List Filter

Filter for a list of devices.

## Structure

`AccountDeviceListFilter`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceIdentifierFilters` | [`List<DeviceIdSearch>`](../../doc/models/device-id-search.md) | Required | Specify the kind of the device identifier, the type of match, and the string that you want to match. | List<DeviceIdSearch> getDeviceIdentifierFilters() | setDeviceIdentifierFilters(List<DeviceIdSearch> deviceIdentifierFilters) |

## Example

```java
import com.verizon.thingspace.models.AccountDeviceListFilter;
import com.verizon.thingspace.models.DeviceIdSearch;
import java.util.Arrays;

AccountDeviceListFilter accountDeviceListFilter = new AccountDeviceListFilter.Builder(
    Arrays.asList(
        new DeviceIdSearch.Builder(
            "4259",
            "iccid"
        )
        .startswith("startswith8")
        .endswith("endswith0")
        .build()
    )
)
.build();
```


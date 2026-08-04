
# Device Extended Diagnostics Result

Result for a request to obtain device extended diagnostics.

## Structure

`DeviceExtendedDiagnosticsResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Categories` | [`List<DiagnosticsCategory>`](../../doc/models/diagnostics-category.md) | Optional | The response includes various types of information about the device, grouped into categories. Each category object contains the category name and a list of Extended Attribute objects as key-value pairs. | List<DiagnosticsCategory> getCategories() | setCategories(List<DiagnosticsCategory> categories) |

## Example

```java
import com.verizon.thingspace.models.CustomFields;
import com.verizon.thingspace.models.DeviceExtendedDiagnosticsResult;
import com.verizon.thingspace.models.DiagnosticsCategory;
import java.util.Arrays;

DeviceExtendedDiagnosticsResult deviceExtendedDiagnosticsResult = new DeviceExtendedDiagnosticsResult.Builder()
    .categories(Arrays.asList(
        new DiagnosticsCategory.Builder()
            .categoryName("Connectivity")
            .extendedAttributes(Arrays.asList(
                new CustomFields.Builder(
                    "Connected",
                    "false"
                )
                .build()
            ))
            .build()
    ))
    .build();
```


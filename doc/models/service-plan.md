
# Service Plan

Details of the service plan.

## Structure

`ServicePlan`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CarrierServicePlanCode` | `String` | Optional | The code that is used by the carrier for the service plan. | String getCarrierServicePlanCode() | setCarrierServicePlanCode(String carrierServicePlanCode) |
| `Code` | `String` | Optional | The code of the service plan, which may not be the same as the name. | String getCode() | setCode(String code) |
| `ExtendedAttributes` | [`List<CustomFields>`](../../doc/models/custom-fields.md) | Optional | Any extended attributes for the service plan, as Key and Value pairs. | List<CustomFields> getExtendedAttributes() | setExtendedAttributes(List<CustomFields> extendedAttributes) |
| `Name` | `String` | Optional | The name of the service plan. | String getName() | setName(String name) |
| `SizeKb` | `Long` | Optional | The size of the service plan in kilobytes. | Long getSizeKb() | setSizeKb(Long sizeKb) |

## Example

```java
import com.verizon.thingspace.models.CustomFields;
import com.verizon.thingspace.models.ServicePlan;
import java.util.Arrays;

ServicePlan servicePlan = new ServicePlan.Builder()
    .carrierServicePlanCode("84638")
    .code("M2MSHR5GB")
    .extendedAttributes(Arrays.asList(
        new CustomFields.Builder(
            "key8",
            "value0"
        )
        .build()
    ))
    .name("2MSHR5GB")
    .sizeKb(0L)
    .build();
```



# Service Plan Responseforplanner

## Structure

`ServicePlanResponseforplanner`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CarrierServicePlanCode` | `String` | Optional | The name of the service plan code | String getCarrierServicePlanCode() | setCarrierServicePlanCode(String carrierServicePlanCode) |
| `Code` | `String` | Optional | The actiavtion code value. | String getCode() | setCode(String code) |
| `ExtendedAttributes` | [`List<KvPairforplanner>`](../../doc/models/kv-pairforplanner.md) | Optional | key/value pairs assigned by the user for filtering.<br><br>**Constraints**: *Maximum Items*: `5` | List<KvPairforplanner> getExtendedAttributes() | setExtendedAttributes(List<KvPairforplanner> extendedAttributes) |
| `Name` | `String` | Optional | The carrier name of the active profile. | String getName() | setName(String name) |
| `SizeKb` | `Integer` | Optional | size in Kilobytes of the service plan | Integer getSizeKb() | setSizeKb(Integer sizeKb) |

## Example

```java
import com.verizon.thingspace.models.KvPairforplanner;
import com.verizon.thingspace.models.ServicePlanResponseforplanner;
import java.util.Arrays;

ServicePlanResponseforplanner servicePlanResponseforplanner = new ServicePlanResponseforplanner.Builder()
    .carrierServicePlanCode("carrierServicePlanCode8")
    .code("code8")
    .extendedAttributes(Arrays.asList(
        new KvPairforplanner.Builder()
            .key("key8")
            .value("value0")
            .build()
    ))
    .name("name0")
    .sizeKb(68)
    .build();
```


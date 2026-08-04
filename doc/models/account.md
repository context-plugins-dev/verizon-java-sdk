
# Account

Returns information about a specified account.

## Structure

`Account`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | The name of the account. | String getAccountName() | setAccountName(String accountName) |
| `AccountNumber` | `String` | Optional | The billing number of the account. | String getAccountNumber() | setAccountNumber(String accountNumber) |
| `OrganizationName` | `String` | Optional | The name of the organization that the account is part of. | String getOrganizationName() | setOrganizationName(String organizationName) |
| `IsProvisioningAllowed` | `Boolean` | Optional | True if devices can be added to the account and activated with a single request. False if devices must be added to the account before they can be activated. | Boolean getIsProvisioningAllowed() | setIsProvisioningAllowed(Boolean isProvisioningAllowed) |
| `Carriers` | `List<String>` | Optional | The names of all carriers for the account. | List<String> getCarriers() | setCarriers(List<String> carriers) |
| `Features` | `List<String>` | Optional | The names of features that are enabled for the account. | List<String> getFeatures() | setFeatures(List<String> features) |
| `IPPools` | [`List<IPPool>`](../../doc/models/ip-pool.md) | Optional | Array of IP pools that are available to the account. | List<IPPool> getIPPools() | setIPPools(List<IPPool> iPPools) |
| `ServicePlans` | [`List<ServicePlan>`](../../doc/models/service-plan.md) | Optional | Array of service plans that are available to the account. | List<ServicePlan> getServicePlans() | setServicePlans(List<ServicePlan> servicePlans) |

## Example

```java
import com.verizon.thingspace.models.Account;
import com.verizon.thingspace.models.IPPool;
import com.verizon.thingspace.models.ServicePlan;
import java.util.Arrays;

Account account = new Account.Builder()
    .accountName("Chintan_CPNStaticBulk")
    .accountNumber("1234567890-77777")
    .organizationName("ChintanCPNBulk")
    .isProvisioningAllowed(true)
    .carriers(Arrays.asList(
        "Verizon Wireless"
    ))
    .features(Arrays.asList(
        "Static IP",
        "Dynamic IP",
        "Customer PN"
    ))
    .iPPools(Arrays.asList(
        new IPPool.Builder()
            .poolName("ACMESTATIC001")
            .poolType("Static IP")
            .isDefaultPool(true)
            .build(),
        new IPPool.Builder()
            .poolName("ACMEDYNAMIC001")
            .poolType("Dynamic IP")
            .isDefaultPool(false)
            .build()
    ))
    .servicePlans(Arrays.asList(
        new ServicePlan.Builder()
            .carrierServicePlanCode("")
            .code("92876")
            .extendedAttributes(Arrays.asList(

            ))
            .name("")
            .sizeKb(1L)
            .build(),
        new ServicePlan.Builder()
            .carrierServicePlanCode("")
            .code("92876")
            .extendedAttributes(Arrays.asList(

            ))
            .name("")
            .sizeKb(1L)
            .build()
    ))
    .build();
```


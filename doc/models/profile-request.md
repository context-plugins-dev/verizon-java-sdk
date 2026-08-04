
# Profile Request

## Structure

`ProfileRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | - | String getAccountName() | setAccountName(String accountName) |
| `Devices` | [`List<DeviceList>`](../../doc/models/device-list.md) | Required | **Constraints**: *Maximum Items*: `100` | List<DeviceList> getDevices() | setDevices(List<DeviceList> devices) |
| `CarrierName` | `String` | Optional | - | String getCarrierName() | setCarrierName(String carrierName) |
| `ServicePlan` | `String` | Optional | - | String getServicePlan() | setServicePlan(String servicePlan) |
| `MdnZipCode` | `String` | Optional | - | String getMdnZipCode() | setMdnZipCode(String mdnZipCode) |
| `PrimaryPlaceOfUse` | [`List<ProfileRequestPrimaryPlaceOfUse>`](../../doc/models/containers/profile-request-primary-place-of-use.md) | Optional | This is List of a container for any-of cases.<br><br>**Constraints**: *Maximum Items*: `25` | List<ProfileRequestPrimaryPlaceOfUse> getPrimaryPlaceOfUse() | setPrimaryPlaceOfUse(List<ProfileRequestPrimaryPlaceOfUse> primaryPlaceOfUse) |
| `SmsrOid` | `String` | Optional | **Constraints**: *Minimum Length*: `3`, *Maximum Length*: `46`, *Pattern*: `^[0-9.]{3,46}$` | String getSmsrOid() | setSmsrOid(String smsrOid) |
| `CarrierIpPoolName` | `String` | Optional | The name of the pool of IP addresses assigned to the profile. | String getCarrierIpPoolName() | setCarrierIpPoolName(String carrierIpPoolName) |

## Example

```java
import com.verizon.thingspace.models.CustomerName;
import com.verizon.thingspace.models.Customernamequery;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceList;
import com.verizon.thingspace.models.ProfileRequest;
import com.verizon.thingspace.models.containers.ProfileRequestPrimaryPlaceOfUse;
import java.util.Arrays;

ProfileRequest profileRequest = new ProfileRequest.Builder(
    "0000123456-00001",
    Arrays.asList(
        new DeviceList.Builder()
            .deviceIds(Arrays.asList(
                new DeviceId.Builder(
                    "id0",
                    "kind8"
                )
                .build()
            ))
            .build()
    )
)
.carrierName("the name of the mobile service provider")
.servicePlan("The service plan name")
.mdnZipCode("five digit zip code")
.primaryPlaceOfUse(Arrays.asList(
        ProfileRequestPrimaryPlaceOfUse.fromCustomernamequery(
            new Customernamequery.Builder()
                .customerName(Arrays.asList(
                    new CustomerName.Builder(
                        "firstName4",
                        "lastName4"
                    )
                    .title("title4")
                    .middleName("middleName8")
                    .suffix("suffix0")
                    .build(),
                    new CustomerName.Builder(
                        "firstName4",
                        "lastName4"
                    )
                    .title("title4")
                    .middleName("middleName8")
                    .suffix("suffix0")
                    .build()
                ))
                .build()
        )
    ))
.smsrOid("smsrOid4")
.build();
```


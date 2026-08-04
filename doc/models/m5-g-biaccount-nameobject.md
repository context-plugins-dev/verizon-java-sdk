
# M5 G Biaccount Nameobject

## Structure

`M5gBiaccountNameobject`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | - | String getAccountName() | setAccountName(String accountName) |
| `BillingCycleEndDate` | `String` | Optional | - | String getBillingCycleEndDate() | setBillingCycleEndDate(String billingCycleEndDate) |
| `CarrierInformation` | [`List<M5gBiCarrierInformation>`](../../doc/models/m5-g-bi-carrier-information.md) | Optional | - | List<M5gBiCarrierInformation> getCarrierInformation() | setCarrierInformation(List<M5gBiCarrierInformation> carrierInformation) |
| `Connected` | `Boolean` | Optional | - | Boolean getConnected() | setConnected(Boolean connected) |
| `CreatedAt` | `String` | Optional | - | String getCreatedAt() | setCreatedAt(String createdAt) |
| `CustomFields` | [`List<M5gBiaccountNameobjectCustomFields>`](../../doc/models/containers/m5-g-biaccount-nameobject-custom-fields.md) | Optional | This is List of a container for any-of cases. | List<M5gBiaccountNameobjectCustomFields> getCustomFields() | setCustomFields(List<M5gBiaccountNameobjectCustomFields> customFields) |
| `DeviceIds` | [`List<M5gBiaccountNameobjectDeviceIds>`](../../doc/models/containers/m5-g-biaccount-nameobject-device-ids.md) | Optional | This is List of a container for any-of cases. | List<M5gBiaccountNameobjectDeviceIds> getDeviceIds() | setDeviceIds(List<M5gBiaccountNameobjectDeviceIds> deviceIds) |
| `ExtendedAttributes` | [`List<M5gBiaccountNameobjectExtendedAttributes>`](../../doc/models/containers/m5-g-biaccount-nameobject-extended-attributes.md) | Optional | This is List of a container for any-of cases. | List<M5gBiaccountNameobjectExtendedAttributes> getExtendedAttributes() | setExtendedAttributes(List<M5gBiaccountNameobjectExtendedAttributes> extendedAttributes) |
| `GroupNames` | [`List<GroupName>`](../../doc/models/group-name.md) | Optional | - | List<GroupName> getGroupNames() | setGroupNames(List<GroupName> groupNames) |
| `Ipaddress` | `String` | Optional | - | String getIpaddress() | setIpaddress(String ipaddress) |
| `LastActivationBy` | `String` | Optional | - | String getLastActivationBy() | setLastActivationBy(String lastActivationBy) |
| `LastActivationDate` | `String` | Optional | - | String getLastActivationDate() | setLastActivationDate(String lastActivationDate) |

## Example

```java
import com.verizon.thingspace.models.M5gBiCarrierInformation;
import com.verizon.thingspace.models.M5gBiaccountNameobject;
import java.util.Arrays;

M5gBiaccountNameobject m5gBiaccountNameobject = new M5gBiaccountNameobject.Builder()
    .accountName("0000123456-00001")
    .billingCycleEndDate("2022-11-10T00:00:00.000Z")
    .carrierInformation(Arrays.asList(
        new M5gBiCarrierInformation.Builder()
            .carrierName("carrierName4")
            .build()
    ))
    .connected(false)
    .createdAt("2022-10-20T18:23:41.000Z")
    .ipaddress("0.0.0.0")
    .lastActivationBy("User Name")
    .lastActivationDate("2022-11-02 T21:36:18Z")
    .build();
```


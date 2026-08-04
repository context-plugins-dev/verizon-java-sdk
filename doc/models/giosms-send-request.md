
# GIOSMS Send Request

## Structure

`GIOSMSSendRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | - | String getAccountName() | setAccountName(String accountName) |
| `CustomFields` | [`List<KvPair>`](../../doc/models/kv-pair.md) | Optional | **Constraints**: *Maximum Items*: `5` | List<KvPair> getCustomFields() | setCustomFields(List<KvPair> customFields) |
| `DataEncoding` | `String` | Optional | - | String getDataEncoding() | setDataEncoding(String dataEncoding) |
| `GroupName` | `String` | Optional | - | String getGroupName() | setGroupName(String groupName) |
| `ServicePlan` | `String` | Optional | - | String getServicePlan() | setServicePlan(String servicePlan) |
| `TimeToLive` | `String` | Optional | A period of time the message remains valid or an end date for the message. This value would be less than the 5 day default. | String getTimeToLive() | setTimeToLive(String timeToLive) |
| `DeviceIds` | [`List<GIODeviceId>`](../../doc/models/gio-device-id.md) | Optional | **Constraints**: *Maximum Items*: `100` | List<GIODeviceId> getDeviceIds() | setDeviceIds(List<GIODeviceId> deviceIds) |
| `SmsMessage` | `String` | Required | - | String getSmsMessage() | setSmsMessage(String smsMessage) |

## Example

```java
import com.verizon.thingspace.models.GIOSMSSendRequest;
import com.verizon.thingspace.models.KvPair;
import java.util.Arrays;

GIOSMSSendRequest gIOSMSSendRequest = new GIOSMSSendRequest.Builder(
    "A text message"
)
.accountName("accountName4")
.customFields(Arrays.asList(
        new KvPair.Builder()
            .key("key0")
            .value("value2")
            .build(),
        new KvPair.Builder()
            .key("key0")
            .value("value2")
            .build()
    ))
.dataEncoding("dataEncoding2")
.groupName("groupName0")
.servicePlan("servicePlan0")
.build();
```


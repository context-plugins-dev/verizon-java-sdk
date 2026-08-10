
# SMS Send Request

Request to send SMS.

## Structure

`SMSSendRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | The name of a billing account. | String getAccountName() | setAccountName(String accountName) |
| `SmsMessage` | `String` | Required | The contents of the SMS message. The SMS message is limited to 160 characters in 7-bit format, or 140 characters in 8-bit format. | String getSmsMessage() | setSmsMessage(String smsMessage) |
| `CustomFields` | [`List<CustomFields>`](../../doc/models/custom-fields.md) | Optional | The names and values of custom fields, if you want to only include devices that have matching custom fields. | List<CustomFields> getCustomFields() | setCustomFields(List<CustomFields> customFields) |
| `DataEncoding` | `String` | Optional | The SMS message encoding, which can be 7-bit (default), 8-bit-ASCII, 8-bit-UTF-8, 8-bit-DATA. | String getDataEncoding() | setDataEncoding(String dataEncoding) |
| `DeviceIds` | [`List<DeviceId>`](../../doc/models/device-id.md) | Optional | The devices that you want to send the message to, specified by device identifier. | List<DeviceId> getDeviceIds() | setDeviceIds(List<DeviceId> deviceIds) |
| `GroupName` | `String` | Optional | The name of a device group, if you want to send the SMS message to all devices in the device group. | String getGroupName() | setGroupName(String groupName) |
| `ServicePlan` | `String` | Optional | The name of a service plan, if you want to only include devices that have that service plan. | String getServicePlan() | setServicePlan(String servicePlan) |
| `TimeToLive` | `String` | Optional | A period of time the message remains valid or an end date for the message. This value would be less than the 5 day default. | String getTimeToLive() | setTimeToLive(String timeToLive) |

## Example

```java
import com.verizon.thingspace.models.CustomFields;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.SMSSendRequest;
import java.util.Arrays;

SMSSendRequest sMSSendRequest = new SMSSendRequest.Builder(
    "accountName6",
    "The rain in Spain stays mainly in the plain."
)
.customFields(Arrays.asList(
        new CustomFields.Builder(
            "key0"
        )
        .value("value2")
        .build(),
        new CustomFields.Builder(
            "key0"
        )
        .value("value2")
        .build(),
        new CustomFields.Builder(
            "key0"
        )
        .value("value2")
        .build()
    ))
.dataEncoding("dataEncoding4")
.deviceIds(Arrays.asList(
        new DeviceId.Builder(
            "id0",
            "kind8"
        )
        .build(),
        new DeviceId.Builder(
            "id0",
            "kind8"
        )
        .build(),
        new DeviceId.Builder(
            "id0",
            "kind8"
        )
        .build()
    ))
.groupName("groupName2")
.servicePlan("T Plan 2")
.build();
```


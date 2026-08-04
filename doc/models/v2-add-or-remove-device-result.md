
# V2 Add or Remove Device Result

Add or remove devices from the existing software upgrade information.

## Structure

`V2AddOrRemoveDeviceResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account identifier. | String getAccountName() | setAccountName(String accountName) |
| `CampaignId` | `String` | Required | Campaign identifier. | String getCampaignId() | setCampaignId(String campaignId) |
| `RequestId` | `String` | Required | Request identifier. | String getRequestId() | setRequestId(String requestId) |

## Example

```java
import com.verizon.thingspace.models.V2AddOrRemoveDeviceResult;

V2AddOrRemoveDeviceResult v2AddOrRemoveDeviceResult = new V2AddOrRemoveDeviceResult.Builder(
    "0402196254-00001",
    "60b5d639-ccdc-4db8-8824-069bd94c95bf",
    "requestId0"
)
.build();
```


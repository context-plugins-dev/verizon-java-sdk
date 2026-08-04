
# Device Id

An identifier for a single device.

## Structure

`DeviceId`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | The value of the device identifier. | String getId() | setId(String id) |
| `Kind` | `String` | Required | The type of the device identifier. Valid types of identifiers are:ESN (decimal),EID,ICCID (up to 20 digits),IMEI (up to 16 digits),MDN,MEID (hexadecimal),MSISDN. | String getKind() | setKind(String kind) |

## Example

```java
import com.verizon.thingspace.models.DeviceId;

DeviceId deviceId = new DeviceId.Builder(
    "990013907835573",
    "imei"
)
.build();
```


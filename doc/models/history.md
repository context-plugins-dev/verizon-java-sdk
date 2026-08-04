
# History

History data for a selected device and its attributes at a specific time.

## Structure

`History`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | The name of the billing account for which you want retrieve history data. An account name is usually numeric, and must include any leading zeros. | String getAccountName() | setAccountName(String accountName) |
| `Device` | [`Device`](../../doc/models/device.md) | Required | Identifies a particular IoT device. | Device getDevice() | setDevice(Device device) |
| `Attributes` | [`HistoryAttributeValue`](../../doc/models/history-attribute-value.md) | Optional | Streaming RF parameter for which you want to retrieve history data. | HistoryAttributeValue getAttributes() | setAttributes(HistoryAttributeValue attributes) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.AttributeIdentifierEnum;
import com.verizon.thingspace.models.Device;
import com.verizon.thingspace.models.History;
import com.verizon.thingspace.models.HistoryAttributeValue;

History history = new History.Builder(
    "0000123456-00001",
    new Device.Builder(
        "15-digit IMEI",
        "IMEI"
    )
    .build()
)
.attributes(new HistoryAttributeValue.Builder()
        .name(AttributeIdentifierEnum.LINK_QUALITY)
        .value("47")
        .createdOn(DateTimeHelper.fromRfc8601DateTime("2022-02-10T16:02:21.406Z"))
        .build())
.build();
```


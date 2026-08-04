
# Check Order Status Request

The request body identifies the devices to upload.

## Structure

`CheckOrderStatusRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | The name of a billing account. An account name is usually numeric, and must include any leading zeros. | String getAccountName() | setAccountName(String accountName) |
| `OrderRequestId` | `String` | Optional | The request id from the activation order. | String getOrderRequestId() | setOrderRequestId(String orderRequestId) |
| `Devices` | [`List<DeviceList>`](../../doc/models/device-list.md) | Required | The devices to upload, specified by device IDs in a format matching uploadType. | List<DeviceList> getDevices() | setDevices(List<DeviceList> devices) |

## Example

```java
import com.verizon.thingspace.models.CheckOrderStatusRequest;
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceList;
import java.util.Arrays;

CheckOrderStatusRequest checkOrderStatusRequest = new CheckOrderStatusRequest.Builder(
    "1223334444-00001",
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
.orderRequestId("f55fea16-3664-4a32-ae9d-c0cbe3eedf1d")
.build();
```


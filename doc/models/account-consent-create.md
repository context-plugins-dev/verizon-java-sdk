
# Account Consent Create

## Structure

`AccountConsentCreate`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceList` | `List<Object>` | Optional | An array of device identifiers | List<Object> getDeviceList() | setDeviceList(List<Object> deviceList) |
| `AccountName` | `String` | Optional | The numeric name of the account, including leading zeros. | String getAccountName() | setAccountName(String accountName) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.AccountConsentCreate;
import java.io.IOException;
import java.util.Arrays;

AccountConsentCreate accountConsentCreate = new AccountConsentCreate.Builder()
    .deviceList(Arrays.asList(
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
    ))
    .accountName("0000123456-00001")
    .build();
```


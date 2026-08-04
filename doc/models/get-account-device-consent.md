
# Get Account Device Consent

## Structure

`GetAccountDeviceConsent`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceList` | `List<Object>` | Optional | An array of device identifiers | List<Object> getDeviceList() | setDeviceList(List<Object> deviceList) |
| `AccountName` | `String` | Optional | The numeric name of the account, including leading zeros. | String getAccountName() | setAccountName(String accountName) |
| `AllDeviceConsent` | `Integer` | Optional | If consent is set at the account level, this value will show the consent level. | Integer getAllDeviceConsent() | setAllDeviceConsent(Integer allDeviceConsent) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.models.GetAccountDeviceConsent;
import java.io.IOException;
import java.util.Arrays;

GetAccountDeviceConsent getAccountDeviceConsent = new GetAccountDeviceConsent.Builder()
    .deviceList(Arrays.asList(
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
    ))
    .accountName("0000123456-00001")
    .allDeviceConsent(1)
    .build();
```



# Location Request

The body contains the the account name and list of devices that you want to locate, plus other options.

## Structure

`LocationRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | Account identifier in "##########-#####". | String getAccountName() | setAccountName(String accountName) |
| `DeviceList` | [`List<DeviceInfo>`](../../doc/models/device-info.md) | Required | Device list. | List<DeviceInfo> getDeviceList() | setDeviceList(List<DeviceInfo> deviceList) |
| `AccuracyMode` | [`AccuracyModeEnum`](../../doc/models/accuracy-mode-enum.md) | Optional | Accurary, currently only 0-coarse supported. | AccuracyModeEnum getAccuracyMode() | setAccuracyMode(AccuracyModeEnum accuracyMode) |
| `CacheMode` | [`CacheModeEnum`](../../doc/models/cache-mode-enum.md) | Optional | Location cache mode. | CacheModeEnum getCacheMode() | setCacheMode(CacheModeEnum cacheMode) |

## Example

```java
import com.verizon.thingspace.models.AccuracyModeEnum;
import com.verizon.thingspace.models.CacheModeEnum;
import com.verizon.thingspace.models.DeviceInfo;
import com.verizon.thingspace.models.LocationRequest;
import java.util.Arrays;

LocationRequest locationRequest = new LocationRequest.Builder(
    "1234567890-00001",
    Arrays.asList(
        new DeviceInfo.Builder(
            "980003420535573",
            "imei",
            "7892345678"
        )
        .build(),
        new DeviceInfo.Builder(
            "375535024300089",
            "imei",
            "7897654321"
        )
        .build(),
        new DeviceInfo.Builder(
            "A100003861E585",
            "meid",
            "7897650914"
        )
        .build()
    )
)
.accuracyMode(AccuracyModeEnum.ENUM_0)
.cacheMode(CacheModeEnum.ENUM_1)
.build();
```


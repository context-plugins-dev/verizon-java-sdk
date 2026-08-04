
# Uploads Activates Device Request

The request body identifies the devices to upload.

## Structure

`UploadsActivatesDeviceRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Required | The name of a billing account. An account name is usually numeric, and must include any leading zeros. | String getAccountName() | setAccountName(String accountName) |
| `EmailAddress` | `String` | Required | The email address that the report should be sent to when the upload is complete. | String getEmailAddress() | setEmailAddress(String emailAddress) |
| `DeviceSku` | `String` | Required | The stock keeping unit that identifies the type of devices in the upload and activation. | String getDeviceSku() | setDeviceSku(String deviceSku) |
| `UploadType` | `String` | Required | The format of the device identifiers in the upload and activation. | String getUploadType() | setUploadType(String uploadType) |
| `ServicePlan` | `String` | Required | The service plan code that you want to assign to all specified devices. | String getServicePlan() | setServicePlan(String servicePlan) |
| `CarrierIpPoolName` | `String` | Optional | The pool from which your device IP addresses is derived. | String getCarrierIpPoolName() | setCarrierIpPoolName(String carrierIpPoolName) |
| `MdnZipCode` | `String` | Required | The Zip code of the location where the line of service is primarily used, or a Zip code that you have been told to use with these devices. | String getMdnZipCode() | setMdnZipCode(String mdnZipCode) |
| `Devices` | [`List<DeviceList>`](../../doc/models/device-list.md) | Required | The devices to upload, specified by device IDs in a format matching uploadType. | List<DeviceList> getDevices() | setDevices(List<DeviceList> devices) |

## Example

```java
import com.verizon.thingspace.models.DeviceId;
import com.verizon.thingspace.models.DeviceList;
import com.verizon.thingspace.models.UploadsActivatesDeviceRequest;
import java.util.Arrays;

UploadsActivatesDeviceRequest uploadsActivatesDeviceRequest = new UploadsActivatesDeviceRequest.Builder(
    "1223334444-00001",
    "bob@mycompany.com",
    "VZW123456",
    "IMEI ICCID Pair",
    "15MBShr",
    "92222",
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
.carrierIpPoolName("The carrier pool name")
.build();
```


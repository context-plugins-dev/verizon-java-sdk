
# Resource Event

## Structure

`ResourceEvent`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountclientid` | `String` | Optional | Not used in this release, future functionality | String getAccountclientid() | setAccountclientid(String accountclientid) |
| `Callbackurl` | `String` | Optional | The URL of the callback listener | String getCallbackurl() | setCallbackurl(String callbackurl) |
| `Createdon` | `LocalDateTime` | Required | Timestamp of the record | LocalDateTime getCreatedon() | setCreatedon(LocalDateTime createdon) |
| `Description` | `String` | Optional | a short description | String getDescription() | setDescription(String description) |
| `Deviceid` | `String` | Optional | This is a UUID value of the device created when the device is onboarded | String getDeviceid() | setDeviceid(String deviceid) |
| `Errmsg` | `String` | Optional | Error message | String getErrmsg() | setErrmsg(String errmsg) |
| `Fieldid` | `String` | Required | - | String getFieldid() | setFieldid(String fieldid) |
| `Fields` | [`DtoFields`](../../doc/models/dto-fields.md) | Optional | Fields to return needed by search | DtoFields getFields() | setFields(DtoFields fields) |
| `Fieldvalue` | `List<Integer>` | Optional | **Constraints**: *Maximum Items*: `100`, `>= 0`, `<= 100` | List<Integer> getFieldvalue() | setFieldvalue(List<Integer> fieldvalue) |
| `Foreignid` | `String` | Required | UUID of the ECPD account the user belongs to | String getForeignid() | setForeignid(String foreignid) |
| `Id` | `String` | Optional | UUID of the user record, assigned at creation | String getId() | setId(String id) |
| `Lastupdated` | `LocalDateTime` | Required | Timestamp of the record | LocalDateTime getLastupdated() | setLastupdated(LocalDateTime lastupdated) |
| `Modelid` | `String` | Optional | The model ID of the device | String getModelid() | setModelid(String modelid) |
| `Name` | `String` | Optional | User defined name of the record | String getName() | setName(String name) |
| `Sensordataaggregation` | `Boolean` | Optional | A flag to indicate if sensor data is to be aggregated (true) or not | Boolean getSensordataaggregation() | setSensordataaggregation(Boolean sensordataaggregation) |
| `State` | `String` | Required | The current status of the device or transaction and will be `success` or `failed` | String getState() | setState(String state) |
| `Transactionid` | `String` | Optional | The system-generated UUID of the transaction | String getTransactionid() | setTransactionid(String transactionid) |
| `Version` | `String` | Optional | The resource version | String getVersion() | setVersion(String version) |
| `Versionid` | `String` | Required | The UUID of the resource version | String getVersionid() | setVersionid(String versionid) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DtoFields;
import com.verizon.thingspace.models.ResourceEvent;

ResourceEvent resourceEvent = new ResourceEvent.Builder(
    DateTimeHelper.fromRfc8601DateTime("2023-10-02T15:46:34.562Z"),
    "The field ID",
    "c1f178d3-eeee-ffff-gggg-0d6b7ae6022a",
    DateTimeHelper.fromRfc8601DateTime("2023-10-02T15:46:34.562Z"),
    "success",
    "337bd2e8-eeee-ffff-gggg-5207992fd395"
)
.accountclientid("null")
.callbackurl("The URL of the callback listener")
.description("a short description")
.deviceid("The UUID of the device")
.errmsg("provider_service_error")
.fields(new DtoFields.Builder()
        .additionalProp1("string")
        .additionalProp2("string")
        .additionalProp3("string")
        .build())
.modelid("The model ID of the device")
.name("name of the record")
.sensordataaggregation(true)
.transactionid("afbcc00d-eeee-ffff-gggg-38b4333fcf06")
.version("1.0")
.build();
```


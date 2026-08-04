
# Resource User

## Structure

`ResourceUser`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Accountclientid` | `String` | Optional | Not used in this release, future functionality | String getAccountclientid() | setAccountclientid(String accountclientid) |
| `Ackterms` | `Boolean` | Optional | Indicates if terms are agreed to (true) or not | Boolean getAckterms() | setAckterms(Boolean ackterms) |
| `Acktermson` | `LocalDateTime` | Optional | - | LocalDateTime getAcktermson() | setAcktermson(LocalDateTime acktermson) |
| `Billingaccountid` | `String` | Optional | The billing account ID. This is the same value as the Account ID | String getBillingaccountid() | setBillingaccountid(String billingaccountid) |
| `Createdon` | `LocalDateTime` | Required | Timestamp of the record | LocalDateTime getCreatedon() | setCreatedon(LocalDateTime createdon) |
| `Credentialsid` | `String` | Optional | User credentials. The only valid value is an email address | String getCredentialsid() | setCredentialsid(String credentialsid) |
| `Credentialstype` | `String` | Required | The type of credential represented by the ID. The only valid value is `email` | String getCredentialstype() | setCredentialstype(String credentialstype) |
| `Customdata` | `Map<String, Object>` | Optional | Name/value pair, where the value is client defined.  The purpose is to keep track of current state per device action. | Map<String, Object> getCustomdata() | setCustomdata(Map<String, Object> customdata) |
| `Description` | `String` | Optional | a short description | String getDescription() | setDescription(String description) |
| `Displayname` | `String` | Optional | the user name value to display | String getDisplayname() | setDisplayname(String displayname) |
| `Email` | `String` | Optional | Contact email for the group | String getEmail() | setEmail(String email) |
| `Firstname` | `String` | Optional | The first name in the user record | String getFirstname() | setFirstname(String firstname) |
| `Foreignid` | `String` | Required | UUID of the ECPD account the user belongs to | String getForeignid() | setForeignid(String foreignid) |
| `Id` | `String` | Optional | UUID of the user record, assigned at creation | String getId() | setId(String id) |
| `Lastname` | `String` | Optional | The last name in the user record | String getLastname() | setLastname(String lastname) |
| `Lastupdated` | `LocalDateTime` | Required | Timestamp of the record | LocalDateTime getLastupdated() | setLastupdated(LocalDateTime lastupdated) |
| `Mdn` | `String` | Optional | The Mobile Directory Number | String getMdn() | setMdn(String mdn) |
| `Middlename` | `String` | Optional | optional field for middle name or initial | String getMiddlename() | setMiddlename(String middlename) |
| `Name` | `String` | Optional | User defined name of the record | String getName() | setName(String name) |
| `Secondarybillingaccountids` | `List<String>` | Optional | Virtual field; will not be used in this implementation<br><br>**Constraints**: *Maximum Items*: `100` | List<String> getSecondarybillingaccountids() | setSecondarybillingaccountids(List<String> secondarybillingaccountids) |
| `State` | `String` | Optional | The current status of the device or transaction and will be `success` or `failed` | String getState() | setState(String state) |
| `Version` | `String` | Optional | The resource version | String getVersion() | setVersion(String version) |
| `Versionid` | `String` | Required | The UUID of the resource version | String getVersionid() | setVersionid(String versionid) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.ResourceUser;

ResourceUser resourceUser = new ResourceUser.Builder(
    DateTimeHelper.fromRfc8601DateTime("2023-10-02T15:46:34.562Z"),
    "email",
    "c1f178d3-eeee-ffff-gggg-0d6b7ae6022a",
    DateTimeHelper.fromRfc8601DateTime("2023-10-02T15:46:34.562Z"),
    "337bd2e8-eeee-ffff-gggg-5207992fd395"
)
.accountclientid("null")
.ackterms(true)
.acktermson(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
.billingaccountid("0000123456-00001")
.credentialsid("email@domain.com")
.description("a short description")
.displayname("User name")
.email("email@domain.com")
.firstname("First name")
.lastname("Last name or Surname")
.mdn("908-555-1234")
.middlename("Middle name or initial")
.name("name of the record")
.state("success")
.version("1.0")
.build();
```


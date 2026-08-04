
# Account Leads Result

Returns information for all leads associated with an account.

## Structure

`AccountLeadsResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HasMoreData` | `Boolean` | Optional | False if no more leads.True if there is more data to be retrieved. | Boolean getHasMoreData() | setHasMoreData(Boolean hasMoreData) |
| `Leads` | [`List<AccountLead>`](../../doc/models/account-lead.md) | Optional | The leads associated with an account. | List<AccountLead> getLeads() | setLeads(List<AccountLead> leads) |

## Example

```java
import com.verizon.thingspace.models.AccountLead;
import com.verizon.thingspace.models.AccountLeadsResult;
import com.verizon.thingspace.models.Address;
import java.util.Arrays;

AccountLeadsResult accountLeadsResult = new AccountLeadsResult.Builder()
    .hasMoreData(false)
    .leads(Arrays.asList(
        new AccountLead.Builder()
            .address(new Address.Builder(
                "1600 Pennsylvania Avenue",
                "Washington",
                "DC",
                "20500",
                "USA"
            )
            .addressLine2("")
            .zip4("zip40")
            .phone("phone4")
            .phoneType("phoneType0")
            .emailAddress("emailAddress6")
            .build())
            .leadId("L-10001")
            .leadState("Qualified")
            .build()
    ))
    .build();
```


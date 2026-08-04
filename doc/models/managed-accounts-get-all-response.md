
# Managed Accounts Get All Response

## Structure

`ManagedAccountsGetAllResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AccountName` | `String` | Optional | Account Name | String getAccountName() | setAccountName(String accountName) |
| `ManagedAccAddedList` | [`List<ManagedAccAddedList>`](../../doc/models/managed-acc-added-list.md) | Optional | - | List<ManagedAccAddedList> getManagedAccAddedList() | setManagedAccAddedList(List<ManagedAccAddedList> managedAccAddedList) |
| `ManagedAccProvisionedList` | [`List<ManagedAccProvisionedList>`](../../doc/models/managed-acc-provisioned-list.md) | Optional | - | List<ManagedAccProvisionedList> getManagedAccProvisionedList() | setManagedAccProvisionedList(List<ManagedAccProvisionedList> managedAccProvisionedList) |

## Example

```java
import com.verizon.thingspace.models.ManagedAccAddedList;
import com.verizon.thingspace.models.ManagedAccProvisionedList;
import com.verizon.thingspace.models.ManagedAccountsGetAllResponse;
import java.util.Arrays;

ManagedAccountsGetAllResponse managedAccountsGetAllResponse = new ManagedAccountsGetAllResponse.Builder()
    .accountName("0212312345-00001")
    .managedAccAddedList(Arrays.asList(
        new ManagedAccAddedList.Builder()
            .id("id6")
            .txid("txid6")
            .build(),
        new ManagedAccAddedList.Builder()
            .id("id6")
            .txid("txid6")
            .build()
    ))
    .managedAccProvisionedList(Arrays.asList(
        new ManagedAccProvisionedList.Builder()
            .id("id2")
            .txid("txid0")
            .build(),
        new ManagedAccProvisionedList.Builder()
            .id("id2")
            .txid("txid0")
            .build()
    ))
    .build();
```



# Upgrade Status Enum

The status of the upgrades that you want to retrieve.

## Enumeration

`UpgradeStatusEnum`

## Fields

| Name |
|  --- |
| `REQUESTPENDING` |
| `QUEUED` |
| `REQUESTFAILED` |
| `INPROGRESS` |
| `FINISHED` |
| `UPGRADEFAILED` |

## Example

```java
import com.verizon.thingspace.models.UpgradeStatusEnum;

UpgradeStatusEnum upgradeStatus = UpgradeStatusEnum.REQUESTFAILED;
```


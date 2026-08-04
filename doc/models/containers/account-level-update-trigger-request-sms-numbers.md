
# Account Level Update Trigger Request Sms Numbers

## Class Name

`AccountLevelUpdateTriggerRequestSmsNumbers`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`Cellphonenumber`](../../../doc/models/cellphonenumber.md) | AccountLevelUpdateTriggerRequestSmsNumbers.fromCellphonenumber(Cellphonenumber cellphonenumber) |

## Cellphonenumber

### Initialization Code

#### Example

```java
AccountLevelUpdateTriggerRequestSmsNumbers.fromCellphonenumber(
        new Cellphonenumber.Builder()
            .number("10-digit mobile number")
            .carrier("mobile service provider")
            .build()
    )
```


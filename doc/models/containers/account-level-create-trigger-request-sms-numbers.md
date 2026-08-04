
# Account Level Create Trigger Request Sms Numbers

## Class Name

`AccountLevelCreateTriggerRequestSmsNumbers`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`Cellphonenumber`](../../../doc/models/cellphonenumber.md) | AccountLevelCreateTriggerRequestSmsNumbers.fromCellphonenumber(Cellphonenumber cellphonenumber) |

## Cellphonenumber

### Initialization Code

#### Example

```java
AccountLevelCreateTriggerRequestSmsNumbers.fromCellphonenumber(
        new Cellphonenumber.Builder()
            .number("10-digit mobile number")
            .carrier("mobile service provider")
            .build()
    )
```


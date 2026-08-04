
# Notificationarray Sms Numbers

## Class Name

`NotificationarraySmsNumbers`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`Cellphonenumber`](../../../doc/models/cellphonenumber.md) | NotificationarraySmsNumbers.fromCellphonenumber(Cellphonenumber cellphonenumber) |

## Cellphonenumber

### Initialization Code

#### Example

```java
NotificationarraySmsNumbers.fromCellphonenumber(
        new Cellphonenumber.Builder()
            .number("10-digit mobile number")
            .carrier("mobile service provider")
            .build()
    )
```


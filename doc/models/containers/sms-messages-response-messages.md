
# Sms Messages Response Messages

## Class Name

`SmsMessagesResponseMessages`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`GIOSmsMessage`](../../../doc/models/gio-sms-message.md) | SmsMessagesResponseMessages.fromGIOSmsMessage(GIOSmsMessage gIOSmsMessage) |

## GIOSmsMessage

### Initialization Code

#### Example

```java
SmsMessagesResponseMessages.fromGIOSmsMessage(
        new GIOSmsMessage.Builder()
            .message("a text message")
            .build()
    )
```



# Client Registration Response

Response for /clients/registration. It provides a generated device ID and the certificates needed to connect the ETX Message Exchange.

## Structure

`ClientRegistrationResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceID` | `UUID` | Required | The generated ID (UUID v4) for the device. It can be used as:<br><br>- the MQTT Client ID when connecting to the Message Exchange system<br>- a parameter when asking for the connection endpoint<br>- a parameter when finishing the device registration<br>- a parameter when unregistering the device | UUID getDeviceID() | setDeviceID(UUID deviceID) |
| `Certificate` | [`Certificate`](../../doc/models/certificate.md) | Required | Structure for the credentials required to connect to the ETX MQTT Message Exchange. | Certificate getCertificate() | setCertificate(Certificate certificate) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.Certificate;
import com.verizon.thingspace.models.ClientRegistrationResponse;
import java.util.UUID;

ClientRegistrationResponse clientRegistrationResponse = new ClientRegistrationResponse.Builder(
    UUID.fromString("a4fcd16a-343d-4527-8203-2f46e3e4ff4b"),
    new Certificate.Builder(
        "\"-----BEGIN CERTIFICATE-----\nMIIDrjCCApagAwIBAgICEAEwDQYJKoZIhvcNAQELBQAwUjELMAkGA1UEBhMCQVUx\n...\nuuA1Zog3aBOeeEzp9SEJBMTJRYPXbK4e8Xer+7m98OL/3g==\n-----END CERTIFICATE-----\"\n",
        "\"-----BEGIN PRIVATE KEY-----\nMIIEvgIBADANBgkqhkiG9w0BAQEFAASCBKgwggSkAgEAAoIBAQDa1lF7DWudshQ5\n...\nJbjD2hacWGzpKzTfn5Mt1frE\n-----END PRIVATE KEY-----\"\n",
        "\"-----BEGIN CERTIFICATE-----\nMIIEvgIBADANBgkqhkiG9w0BAQEFAASCBKgwggSkAgEAAoIBAQDa1lF7DWudshQ5\n...\nJbjD2hacWGzpKzTfn5Mt1frE\n-----END CERTIFICATE-----\"\n",
        DateTimeHelper.fromRfc8601DateTime("2017-07-21T17:32:28Z")
    )
    .build()
)
.build();
```


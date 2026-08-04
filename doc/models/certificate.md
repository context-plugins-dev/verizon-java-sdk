
# Certificate

Structure for the credentials required to connect to the ETX MQTT Message Exchange.

## Structure

`Certificate`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CertPem` | `String` | Required | The string containing the certificate<br><br>**Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096`, *Pattern*: ``^[a-zA-Z0-9~\+\-!@#$%^&*()\`\[\]{=};\"':,.\/<>?\|\s]+$`` | String getCertPem() | setCertPem(String certPem) |
| `KeyPem` | `String` | Required | The string containing the private key<br><br>**Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096`, *Pattern*: ``^[a-zA-Z0-9~\+\-!@#$%^&*()\`\[\]{=};\"':,.\/<>?\|\s]+$`` | String getKeyPem() | setKeyPem(String keyPem) |
| `CaPem` | `String` | Required | The string containing the CA certificate<br><br>**Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096`, *Pattern*: ``^[a-zA-Z0-9~\+\-!@#$%^&*()\`\[\]{=};\"':,.\/<>?\|\s]+$`` | String getCaPem() | setCaPem(String caPem) |
| `ExpirationTime` | `LocalDateTime` | Required | The string describing the expiration timestamp of the certificate | LocalDateTime getExpirationTime() | setExpirationTime(LocalDateTime expirationTime) |

## Example

```java
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.Certificate;

Certificate certificate = new Certificate.Builder(
    "\"-----BEGIN CERTIFICATE-----\nMIIDrjCCApagAwIBAgICEAEwDQYJKoZIhvcNAQELBQAwUjELMAkGA1UEBhMCQVUx\n...\nuuA1Zog3aBOeeEzp9SEJBMTJRYPXbK4e8Xer+7m98OL/3g==\n-----END CERTIFICATE-----\"\n",
    "\"-----BEGIN PRIVATE KEY-----\nMIIEvgIBADANBgkqhkiG9w0BAQEFAASCBKgwggSkAgEAAoIBAQDa1lF7DWudshQ5\n...\nJbjD2hacWGzpKzTfn5Mt1frE\n-----END PRIVATE KEY-----\"\n",
    "\"-----BEGIN CERTIFICATE-----\nMIIEvgIBADANBgkqhkiG9w0BAQEFAASCBKgwggSkAgEAAoIBAQDa1lF7DWudshQ5\n...\nJbjD2hacWGzpKzTfn5Mt1frE\n-----END CERTIFICATE-----\"\n",
    DateTimeHelper.fromRfc8601DateTime("2017-07-21T17:32:28Z")
)
.build();
```


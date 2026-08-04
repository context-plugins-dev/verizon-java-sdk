
# Auth Rest Error Responseforplanner Exception

## Structure

`AuthRestErrorResponseforplannerException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Fault` | [`AuthSubRestErrorResponseforplanner`](../../doc/models/auth-sub-rest-error-responseforplanner.md) | Optional | - | AuthSubRestErrorResponseforplanner getFault() | setFault(AuthSubRestErrorResponseforplanner fault) |

## Example

```java
try {
    // make the API call
} catch (AuthRestErrorResponseforplannerException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```


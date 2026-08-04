
# Sensor Insights Device Action Set Request Body

## Class Name

`SensorInsightsDeviceActionSetRequestBody`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`DtoDeviceActionSetRequest`](../../../doc/models/dto-device-action-set-request.md) | SensorInsightsDeviceActionSetRequestBody.fromDtoDeviceActionSetRequest(DtoDeviceActionSetRequest dtoDeviceActionSetRequest) |
| [`DtoDeviceCommand`](../../../doc/models/dto-device-command.md) | SensorInsightsDeviceActionSetRequestBody.fromDtoDeviceCommand(DtoDeviceCommand dtoDeviceCommand) |

## DtoDeviceActionSetRequest

### Initialization Code

#### Example

```java
SensorInsightsDeviceActionSetRequestBody.fromDtoDeviceActionSetRequest(
        new DtoDeviceActionSetRequest.Builder()
            .accountname("0000123456-00001")
            .build()
    )
```

## DtoDeviceCommand

### Initialization Code

#### Example

```java
SensorInsightsDeviceActionSetRequestBody.fromDtoDeviceCommand(
        new DtoDeviceCommand.Builder()
            .accountName("0000123456-00001")
            .build()
    )
```


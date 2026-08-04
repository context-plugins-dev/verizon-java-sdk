
# Delete Devices Result Device Ids

## Class Name

`DeleteDevicesResultDeviceIds`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`List<DeviceId>`](../../../doc/models/device-id.md) | DeleteDevicesResultDeviceIds.fromListOfDeviceId(List<DeviceId> listOfDeviceId) |
| [`DeviceId`](../../../doc/models/device-id.md) | DeleteDevicesResultDeviceIds.fromDeviceId(DeviceId deviceId) |

## List<DeviceId>

### Initialization Code

#### Example

```java
DeleteDevicesResultDeviceIds.fromListOfDeviceId(
        Arrays.asList(
            new DeviceId.Builder(
                "09005470263",
                "esn"
            )
            .build()
        )
    )
```

## DeviceId

### Initialization Code

#### Example

```java
DeleteDevicesResultDeviceIds.fromDeviceId(
        new DeviceId.Builder(
            "990013907835573",
            "imei"
        )
        .build()
    )
```


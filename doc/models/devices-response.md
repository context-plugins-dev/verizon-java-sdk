
# Devices Response

Device information containing ID, type classification, and associated MEC IDs

## Structure

`DevicesResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeviceID` | `UUID` | Required | The generated ID (UUID v4) for the device. It can be used as:<br><br>- the MQTT Client ID when connecting to the Message Exchange system<br>- a parameter when asking for the connection endpoint<br>- a parameter when finishing the device registration<br>- a parameter when unregistering the device | UUID getDeviceID() | setDeviceID(UUID deviceID) |
| `ClientType` | [`EtxClientTypeEnum`](../../doc/models/etx-client-type-enum.md) | Required | The type of the client that is to be registered. This is one of the major traffic participant groups considered in V2X communication. The system uses this value to define which topics the client will be able to publish and subscribe to.<br><br>Values:<br><br>- **Vehicle** - Vehicle with an enclosure around the passengers. (Subtypes: Motorcycle, PassengerCar, Truck, Bus, EmergencyVehicle, SchoolBus, MaintenanceVehicle)<br>- **VulnerableRoadUser** - Traffic participants without a protecting enclosure. (Subtypes: Bicycle, Pedestrian, Scooter)<br>- **TrafficLightController** - A Traffic light controller system. (Subtypes: NA)<br>- **InfrastructureSensor** - Sensors that are deployed in the infrastructure. (Subtypes: RoadSideUnit, Camera, Lidar, Radar, InductiveLoop, MagneticSensor)<br>- **OnboardSensor** - Sensors that are onboard on a vehicle(Subtypes: Camera, Lidar, Radar)<br>- **Software** - A software system or application. (Subtypes: Platform, Application, NA) | EtxClientTypeEnum getClientType() | setClientType(EtxClientTypeEnum clientType) |
| `ClientSubtype` | [`ClientSubtypeEnum`](../../doc/models/client-subtype-enum.md) | Required | The subtype or subgroup of the client type. This further specifies the client type. For example it will specify if the client is a passenger car or a truck. See the ClientType description for the supported Subtypes for each client type. | ClientSubtypeEnum getClientSubtype() | setClientSubtype(ClientSubtypeEnum clientSubtype) |
| `MecIds` | `List<String>` | Required | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10`, *Maximum Length*: `128`, *Pattern*: `^[a-z0-9\-]+$` | List<String> getMecIds() | setMecIds(List<String> mecIds) |

## Example

```java
import com.verizon.thingspace.models.ClientSubtypeEnum;
import com.verizon.thingspace.models.DevicesResponse;
import com.verizon.thingspace.models.EtxClientTypeEnum;
import java.util.Arrays;
import java.util.UUID;

DevicesResponse devicesResponse = new DevicesResponse.Builder(
    UUID.fromString("a4fcd16a-343d-4527-8203-2f46e3e4ff4b"),
    EtxClientTypeEnum.VEHICLE,
    ClientSubtypeEnum.MAGNETICSENSOR,
    Arrays.asList(
        "MecIds1",
        "MecIds0",
        "MecIds9"
    )
)
.build();
```


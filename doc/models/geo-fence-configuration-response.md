
# Geo Fence Configuration Response

Response for /api/v1/application/configurations/geofence endpoint. It provides a response if the configuration was created and saved in the system.

## Structure

`GeoFenceConfigurationResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | The generated ID (UUID v4) for the configuration. It has to be used when asking for changing any of the configuration parameters.<br><br>**Constraints**: *Minimum Length*: `32`, *Maximum Length*: `36`, *Pattern*: `^[0-9a-fA-F]{8}-?[0-9a-fA-F]{4}-?4[0-9a-fA-F]{3}-?[89abAB][0-9a-fA-F]{3}-?[0-9a-fA-F]{12}$` | String getId() | setId(String id) |
| `VendorId` | `String` | Required | The vendor that the configuration belongs to. E.g. Verizon, GM, Ford, etc.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]+$` | String getVendorId() | setVendorId(String vendorId) |
| `Name` | `String` | Optional | Name of the configuration.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: ``^[\w\+\-!()\`\[\]{=};\"':,.\/<>?\|\s]+$`` | String getName() | setName(String name) |
| `Description` | `String` | Optional | Description of the configuration.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `2048`, *Pattern*: ``^[\w\+\-!()\`\[\]{=};\"':,.\/<>?\|\s]+$`` | String getDescription() | setDescription(String description) |
| `GeoFence` | [`GeoFence`](../../doc/models/geo-fence.md) | Required | The GeoJSON representation of geofence. Geofence supports the following geometry types: LineString, Polygon, MultiLineString, and MultiPolygon. The system only supports a single Feature in the FeatureCollection, so only one Line, Polygon, MultiLine or MultiPolygon can be defined within one Geofencing configuration. | GeoFence getGeoFence() | setGeoFence(GeoFence geoFence) |
| `MessageStandard` | [`MessageStandardEnum`](../../doc/models/message-standard-enum.md) | Required | Select which V2X messaging standard will be used for the message generation. The following options are supported:<br><br>- "etsi": The message will be generated using the ETSI (European) standard (e.g. DENM).<br>- "sae": The message will be generated using the SAE J2735 (North American) standard (e.g. RSA, TIM).<br>- if not sent while POST, defaults to "sae"<br>- mandatory to send "etsi" standard here, if ETSI messages are being sent in config<br><br>**Default**: `MessageStandardEnum.SAE` | MessageStandardEnum getMessageStandard() | setMessageStandard(MessageStandardEnum messageStandard) |
| `Messages` | [`List<Message4>`](../../doc/models/containers/message-4.md) | Required | List of predefined messages that belongs to the geofence. These are the messages that are sent out by the system when the Trigger Condition for the message is met.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `10` | List<Message4> getMessages() | setMessages(List<Message4> messages) |
| `IsActive` | `boolean` | Required | - | boolean getIsActive() | setIsActive(boolean isActive) |

## Example

```java
import com.verizon.thingspace.ApiHelper;
import com.verizon.thingspace.DateTimeHelper;
import com.verizon.thingspace.models.DistributionSchedule;
import com.verizon.thingspace.models.DistributionTypesEnum;
import com.verizon.thingspace.models.FeatureItem;
import com.verizon.thingspace.models.GenericPayload;
import com.verizon.thingspace.models.GeoFence;
import com.verizon.thingspace.models.GeoFenceConfigurationResponse;
import com.verizon.thingspace.models.LineString;
import com.verizon.thingspace.models.Message;
import com.verizon.thingspace.models.MessageStandardEnum;
import com.verizon.thingspace.models.RoadUserTypesEnum;
import com.verizon.thingspace.models.SpeedItem;
import com.verizon.thingspace.models.SpeedRange;
import com.verizon.thingspace.models.TriggerConditionEnum;
import com.verizon.thingspace.models.Type1Enum;
import com.verizon.thingspace.models.Type2Enum;
import com.verizon.thingspace.models.TypeEnum;
import com.verizon.thingspace.models.containers.Geometry;
import com.verizon.thingspace.models.containers.Limits;
import com.verizon.thingspace.models.containers.Message4;
import java.io.IOException;
import java.util.Arrays;

GeoFenceConfigurationResponse geoFenceConfigurationResponse = new GeoFenceConfigurationResponse.Builder(
    "a4fcd16a-343d-4527-8203-2f46e3e4ff4b",
    "VerizonETX",
    new GeoFence.Builder(
        TypeEnum.FEATURECOLLECTION,
        Arrays.asList(
            new FeatureItem.Builder(
                Type1Enum.FEATURE,
                Geometry.fromLineString(
                    new LineString.Builder(
                        Type2Enum.LINESTRING,
                        Arrays.asList(
                            Arrays.asList(
                                51.53D,
                                51.54D
                            ),
                            Arrays.asList(
                                51.53D,
                                51.54D
                            )
                        )
                    )
                    .build()
                ),
                ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
            )
            .build()
        )
    )
    .build(),
    MessageStandardEnum.SAE,
    Arrays.asList(
        Message4.fromMessage(
            new Message.Builder(
                false,
                Arrays.asList(
                    RoadUserTypesEnum.VULNERABLEROADUSER
                ),
                Arrays.asList(
                    TriggerConditionEnum.CROSSING
                ),
                new GenericPayload.Builder(
                    "messageType4",
                    "messageFormat6",
                    "payload0"
                )
                .build()
            )
            .limits(Arrays.asList(
                    Limits.fromSpeedItem(
                        new SpeedItem.Builder(
                            new SpeedRange.Builder(
                                64.76D,
                                138.18D
                            )
                            .build()
                        )
                        .build()
                    )
                ))
            .distributionType(Arrays.asList(
                    DistributionTypesEnum.BROADCAST,
                    DistributionTypesEnum.TARGETED
                ))
            .distributionSchedule(new DistributionSchedule.Builder(
                    90,
                    88
                )
                .startTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .build())
            .build()
        ),
        Message4.fromMessage(
            new Message.Builder(
                false,
                Arrays.asList(
                    RoadUserTypesEnum.VULNERABLEROADUSER
                ),
                Arrays.asList(
                    TriggerConditionEnum.CROSSING
                ),
                new GenericPayload.Builder(
                    "messageType4",
                    "messageFormat6",
                    "payload0"
                )
                .build()
            )
            .limits(Arrays.asList(
                    Limits.fromSpeedItem(
                        new SpeedItem.Builder(
                            new SpeedRange.Builder(
                                64.76D,
                                138.18D
                            )
                            .build()
                        )
                        .build()
                    )
                ))
            .distributionType(Arrays.asList(
                    DistributionTypesEnum.BROADCAST,
                    DistributionTypesEnum.TARGETED
                ))
            .distributionSchedule(new DistributionSchedule.Builder(
                    90,
                    88
                )
                .startTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .build())
            .build()
        )
    ),
    false
)
.name("name2")
.description("description2")
.build();
```


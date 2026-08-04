
# Message 4

## Class Name

`Message4`

## Cases

| Type | Factory Method |
|  --- | --- |
| [`Message`](../../../doc/models/message.md) | Message4.fromMessage(Message message) |
| [`Message1`](../../../doc/models/message-1.md) | Message4.fromMessage1(Message1 message1) |
| [`Message2`](../../../doc/models/message-2.md) | Message4.fromMessage2(Message2 message2) |
| [`Message3`](../../../doc/models/message-3.md) | Message4.fromMessage3(Message3 message3) |

## Message

### Initialization Code

#### Example

```java
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
        .build()
    )
```

## Message1

### Initialization Code

#### Example

```java
Message4.fromMessage1(
        new Message1.Builder(
            false,
            Arrays.asList(
                RoadUserTypesEnum.VULNERABLEROADUSER,
                RoadUserTypesEnum.VEHICLE,
                RoadUserTypesEnum.VULNERABLEROADUSER
            ),
            Arrays.asList(
                TriggerConditionEnum.CROSSING,
                TriggerConditionEnum.ENTER
            ),
            new SaeAlertPayload.Builder(
                160
            )
            .msgCnt(0)
            .build()
        )
        .build()
    )
```

## Message2

### Initialization Code

#### Example

```java
Message4.fromMessage2(
        new Message2.Builder(
            false,
            Arrays.asList(
                RoadUserTypesEnum.VULNERABLEROADUSER,
                RoadUserTypesEnum.VEHICLE
            ),
            Arrays.asList(
                TriggerConditionEnum.CROSSING,
                TriggerConditionEnum.ENTER,
                TriggerConditionEnum.LEAVE
            ),
            new SaeInfoPayload.Builder(
                Arrays.asList(
                    new DataFrame.Builder(
                        FrameTypeEnum.UNKNOWN,
                        DataFrameMsgId.fromFurtherInfoMsgId(
                            new FurtherInfoMsgId.Builder(
                                "1101"
                            )
                            .build()
                        ),
                        186,
                        44,
                        7,
                        Arrays.asList(
                            new GeographicalPath.Builder()
                                .direction("1101")
                                .build()
                        ),
                        DataFrameContent.fromAdvisoryContent(
                            new AdvisoryContent.Builder(
                                Arrays.asList(
                                    AdvisoryItem.fromITISItemWrapper(
                                        new ITISItemWrapper.Builder(
                                            new ITISItemContent.Builder(
                                                10
                                            )
                                            .build()
                                        )
                                        .build()
                                    )
                                )
                            )
                            .build()
                        )
                    )
                    .doNotUse1(0)
                    .doNotUse2(0)
                    .doNotUse3(0)
                    .doNotUse4(0)
                    .build()
                )
            )
            .msgCnt(0)
            .timeStamp(5)
            .packetID("B343B343B343B343A5")
            .urlB("http://example.com")
            .build()
        )
        .build()
    )
```

## Message3

### Initialization Code

#### Example

```java
Message4.fromMessage3(
        new Message3.Builder(
            false,
            Arrays.asList(
                RoadUserTypesEnum.VULNERABLEROADUSER,
                RoadUserTypesEnum.VEHICLE
            ),
            Arrays.asList(
                TriggerConditionEnum.LEAVE,
                TriggerConditionEnum.INSIDE
            ),
            new EtsiAlertPayload.Builder(
                new Header.Builder(
                    ProtocolVersionEnum.ENUM_2,
                    MessageIdEnum.ENUM_1,
                    12345
                )
                .build(),
                new DenmPayload.Builder(
                    new Management.Builder(
                        new ActionId.Builder(
                            28,
                            42
                        )
                        .build(),
                        123456789L,
                        123456789L,
                        new EventPosition.Builder(
                            198,
                            234,
                            new PosConfidenceEllipse.Builder(
                                16,
                                114,
                                100
                            )
                            .build(),
                            new Altitude.Builder()
                                .build()
                        )
                        .build(),
                        148
                    )
                    .build()
                )
                .build()
            )
            .build()
        )
        .build()
    )
```


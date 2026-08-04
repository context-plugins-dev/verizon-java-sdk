
# Frame Type Enum

The frameType data element provides the type of message to follow in the rest of the message frame structure. The following frame types are supported:

- unknown
- advisory
- roadSignage
- commercialSignage

## Enumeration

`FrameTypeEnum`

## Fields

| Name |
|  --- |
| `UNKNOWN` |
| `ADVISORY` |
| `ROADSIGNAGE` |
| `COMMERCIALSIGNAGE` |

## Example

```java
import com.verizon.thingspace.models.FrameTypeEnum;

FrameTypeEnum frameType = FrameTypeEnum.UNKNOWN;
```


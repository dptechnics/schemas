# Equipment Schema

```txt
https://poseidat.org/schema/core/equipment/equipment.json#/properties/equipment/items
```

A piece of equipment installed on a vessel. Equipment is composed out of different devices


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                  |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [equipment-inventory.json\*](schemas/entry/equipment-inventory.json "open original schema") |

## items Type

`object` ([Equipment](equipment-inventory-properties-equipment-on-board-equipment.md))

# Equipment Properties

| Property                  | Type     | Required | Nullable       | Defined by                                                                                                                        |
| :------------------------ | -------- | -------- | -------------- | :-------------------------------------------------------------------------------------------------------------------------------- |
| [id](#id)                 | `string` | Required | cannot be null | [Equipment](equipment-properties-id.md "https&#x3A;//poseidat.org/schema/core/equipment/equipment.json#/properties/id")           |
| [name](#name)             | `string` | Required | cannot be null | [Equipment](equipment-properties-name.md "https&#x3A;//poseidat.org/schema/core/equipment/equipment.json#/properties/name")       |
| [type](#type)             | `string` | Required | cannot be null | [Equipment](equipment-properties-equipment-type.md "https&#x3A;//poseidat.org/schema/enum/equipment-type.json#/properties/type")  |
| [supplier](#supplier)     | `object` | Optional | cannot be null | [Equipment](equipment-properties-company.md "https&#x3A;//poseidat.org/schema/core/persona/company.json#/properties/supplier")    |
| [installer](#installer)   | `object` | Optional | cannot be null | [Equipment](equipment-properties-company.md "https&#x3A;//poseidat.org/schema/core/persona/company.json#/properties/installer")   |
| [maintainer](#maintainer) | `object` | Optional | cannot be null | [Equipment](equipment-properties-company.md "https&#x3A;//poseidat.org/schema/core/persona/company.json#/properties/maintainer")  |
| [devices](#devices)       | `array`  | Required | cannot be null | [Equipment](equipment-properties-devices.md "https&#x3A;//poseidat.org/schema/core/equipment/equipment.json#/properties/devices") |

## id

The unique identifier for the equipment (UUID v4)


`id`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [Equipment](equipment-properties-id.md "https&#x3A;//poseidat.org/schema/core/equipment/equipment.json#/properties/id")

### id Type

`string`

### id Constraints

**UUID**: the string must be a UUID, according to [RFC 4122](https://tools.ietf.org/html/rfc4122 "check the specification")

## name

Name of the equipment


`name`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [Equipment](equipment-properties-name.md "https&#x3A;//poseidat.org/schema/core/equipment/equipment.json#/properties/name")

### name Type

`string`

## type

The types of supported technical vessel equipment.


`type`

-   is required
-   Type: `string` ([Equipment type](equipment-properties-equipment-type.md))
-   cannot be null
-   defined in: [Equipment](equipment-properties-equipment-type.md "https&#x3A;//poseidat.org/schema/enum/equipment-type.json#/properties/type")

### type Type

`string` ([Equipment type](equipment-properties-equipment-type.md))

### type Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value              | Explanation |
| :----------------- | ----------- |
| `"ENGINE"`         |             |
| `"GNSS"`           |             |
| `"ECHOSOUNDER"`    |             |
| `"FISHFINDER"`     |             |
| `"AIS"`            |             |
| `"ECONOMETER"`     |             |
| `"TANKLEVELMETER"` |             |
| `"TENSIOMETER"`    |             |
| `"CHARGER"`        |             |
| `"SEPARATOR"`      |             |
| `"COMPASS"`        |             |
| `"VSAT"`           |             |
| `"REFRIDGERATOR"`  |             |
| `"ICEMAKER"`       |             |
| `"WINCH"`          |             |
| `"RUDDER"`         |             |
| `"PROPELLER"`      |             |
| `"PUMP"`           |             |
| `"SENSOR"`         |             |

## supplier

A company involved with the vessel


`supplier`

-   is optional
-   Type: `object` ([Company](equipment-properties-company.md))
-   cannot be null
-   defined in: [Equipment](equipment-properties-company.md "https&#x3A;//poseidat.org/schema/core/persona/company.json#/properties/supplier")

### supplier Type

`object` ([Company](equipment-properties-company.md))

## installer

A company involved with the vessel


`installer`

-   is optional
-   Type: `object` ([Company](equipment-properties-company.md))
-   cannot be null
-   defined in: [Equipment](equipment-properties-company.md "https&#x3A;//poseidat.org/schema/core/persona/company.json#/properties/installer")

### installer Type

`object` ([Company](equipment-properties-company.md))

## maintainer

A company involved with the vessel


`maintainer`

-   is optional
-   Type: `object` ([Company](equipment-properties-company.md))
-   cannot be null
-   defined in: [Equipment](equipment-properties-company.md "https&#x3A;//poseidat.org/schema/core/persona/company.json#/properties/maintainer")

### maintainer Type

`object` ([Company](equipment-properties-company.md))

## devices

The collection of devices of which this equipment is composed


`devices`

-   is required
-   Type: `object[]` ([Device](equipment-properties-devices-device.md))
-   cannot be null
-   defined in: [Equipment](equipment-properties-devices.md "https&#x3A;//poseidat.org/schema/core/equipment/equipment.json#/properties/devices")

### devices Type

`object[]` ([Device](equipment-properties-devices-device.md))

### devices Constraints

**minimum number of items**: the minimum number of items for this array is: `2`
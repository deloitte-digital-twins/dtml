# Digital Twin Modeling Language

The Digital Twins Modeling Language (DTML) is a specification for defining digital twin models of IoT devices. Any device manufacturer can create, publish and manage digital twin models for their devices, parts and components using DTML in no time.

DTML is open to the community and Deloitte encourages collaboration with clients, industry, and manufacturers. It is based on open JSON format allowing for quicker adoption.

## Models
Models are used to define the structure and schema of Digital Twin Entities, Components, and Devices (often times, these may be the same). Each JSON file represents an individual model.  Models can be instantiated into actual instances of Digital Twins. They are also used in Deloitte's IoT Telemetry Simulator for purposes such as generating device-specific synthetic telemetry messages for rapid experimentation, development and testing.

Basic DTML Structure:

```
{
	"twinId": "",
	"properties": {
		"PROPERTY_1": {
			"type": "DATA TYPE"
		},
    "PROPERTY_2": {
      "type": "DATA TYPE"
    }
	}
}

```

DTML Example:

```
{
	"twinId": "",
	"properties": {
		"charge": {
			"type": "float"
		},
		"voltage": {
			"type": "float"
		}
	}
}
```

The data types indicated by the `type` property may be any valid property data type.  At this time they are the following:
- integer
- float
- string
- boolean
- point
- date
- time
- localtime
- datetime
- localdatetime
- duration

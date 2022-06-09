### Models
Models are used to define the structure and schema of Digital Twin Entities, Components, and Devices (often times, these may be the same).  These Models are defined via _**Digital Twins Modeling Language**_ (_**DTML**_).  DTML is a JSON-based modeling language, where each JSON file represents an individual model.  Models can be instantiated into actual instances of Digital Twins.  They are also used by this simulator for purposes such as generating device-specific telemetry messages.

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

The data types indicated by the `type` property may be any valid neo4j property data type.  At this time they are the following:
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

For documentation on neo4j datatypes, see link: <https://neo4j.com/docs/cypher-manual/current/syntax/values/>

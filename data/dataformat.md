**README**

# GeoEngine Data Format

## v0.0

The GeoEngine data format is a JSON-based format for representing geospatial data. It is designed to be simple and easy to use, while still being flexible enough to support a wide range of geospatial data types.

The GeoEngine data format consists of a nested array of objects, creating a 3D matrix representing i (planner x-axis) x j (planner y-axis) x t (time). The measure property or feature is represented as object.

The feature object must contain the following properties:

* `point`: A GeoJSON point object representing the location of the feature.
* `property`: A string representing the name of the property associated with the feature.
* `value`: An array of values for the property.
* `boundingPoints`: A GeoJSON polygon object representing the bounding box of the feature.

The following is an example of a GeoEngine data format object:

```json
{
  "point": {
    "long": 22.2432647,
    "lat": 60.24324642
  },
  "property": "CO2 Concentration",
  "value": [200],
  "boundingPoints": [
    {
      "long": 22.2432632,
      "lat": 60.24324634
    },
    {
      "long": 22.2432642,
      "lat": 60.24324634
    },
    {
      "long": 22.2432632,
      "lat": 60.24324657
    },
    {
      "long": 22.2432642,
      "lat": 60.24324657
    }
  ]
}
```

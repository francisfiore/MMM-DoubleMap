# MMM-DoubleMap

This is a module for the [MagicMirror²](https://github.com/MichMich/MagicMirror/).

This Magic Mirror module provides a Magic Mirror UI and configuration for any bus system which uses DoubleMap to allow its users to interact with the bus system in a live capacity.

## Using the module

To use this module, add the following configuration block to the modules array in the `config/config.js` file:
```js
var config = {
    modules: [
        {
            module: 'MMM-DoubleMap',
            config: {
                organization: "",
                originLat: "",
                originLon: "",
                originRadius: "",
                destLat: "",
                destLon: "",
                destRadius: "",
                theme: ""
            }
        }
    ]
}
```

## Configuration options

| Option           | Required   | Description
|----------------- |----------- |-----------
| `organization`   | *Required* | The organization id for double.<br><br>**Type:** `string` <br>Example: for https://mbus.doublemap.com/, organization='mbus'
| `originLat`      | *Required* | The latitude of the origin point from which the nearest bus stops will be found. <br><br>**Type:**`float`
| `originLon`      | *Required* | The longitude of the origin point from which the nearest bus stops will be found. <br><br>**Type:**`float`
| `originRadius`   | *Optional* | Walking radius, in minutes, from the origin position to find bus stops. <br><br>**Type:** `int`(minutes) <br>Default 5 minutes
| `destLat`        | *Optional* | The latitude of the destination point from which the nearest bus stops will be found. <br><br>**Type:**`float`
| `destLon`        | *Optional* | The longitude of the destination point from which the nearest bus stops will be found. <br><br>**Type:**`float`
| `destRadius`     | *Optional* | Walking radius, in minutes, from the destination position to find bus stops. If no bus stops are found within the radius around the destination that follow bus stops within the radius of the origin, no routes will be displayed.<br><br>**Type:** `int`(minutes) <br>Default 5 minutes
| `theme`          | *Optional* | Map and module display theme.<br><br>**Type:**`string`<br>Default `light`. Currently supports `dark` and `light`

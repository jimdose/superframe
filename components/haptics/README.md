## aframe-haptics-component

[![Version](http://img.shields.io/npm/v/aframe-haptics-component.svg?style=flat-square)](https://npmjs.org/package/aframe-haptics-component)
[![License](http://img.shields.io/npm/l/aframe-haptics-component.svg?style=flat-square)](https://npmjs.org/package/aframe-haptics-component)

A controller haptics (vibrations) component for A-Frame. Supported by
experimental [Gamepad
Extensions](https://w3c.github.io/gamepad/extensions.html#dom-gamepadhapticactuator). [Read about browser support](https://developer.mozilla.org/en-US/docs/Web/API/Gamepad/hapticActuators).

For [A-Frame](https://aframe.io).

### API

| Property      | Description                                                                                            | Default Value |
| --------      | -----------                                                                                            | ------------- |
| actuatorIndex | Index of the actuator from the gamepad's array of actuators.                                           | 0             |
| dur           | Duration of vibration pulse (milliseconds).                                                            | 100           |
| enabled       | Whether the component should pulse on the event.                                                       | true          |
| events        | Array of events for controller entity to listen to to trigger a pulse (e.g., `triggerdown, triggerup`) | []            |
| intensity     | Intensity of pulse (from 0 to 1)                                                                       | 1             |

### Installation

#### Browser

Install and use by directly including the [browser files](dist):

```html
<head>
  <title>My A-Frame Scene</title>
  <script src="https://aframe.io/releases/0.7.0/aframe.min.js"></script>
  <script src="https://unpkg.com/aframe-haptics-component/dist/aframe-haptics-component.min.js"></script>
</head>

<body>
  <a-scene>
    <a-entity hand-controls="left"  haptics="events: triggerdown; dur: 1000; intensity: 0.5"></a-entity>
    <a-entity hand-controls="right" haptics="events: triggerdown; dur: 500; intensity: 1"></a-entity>
  </a-scene>
</body>
```

#### npm

Install via npm:

```bash
npm install aframe-haptics-component
```

Then require and use.

```js
require('aframe');
require('aframe-haptics-component');
```
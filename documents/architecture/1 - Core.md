# Core

Translating units for input and output is job of the User Interface.

## Units

`angle: Integer` - *from the robots position in the environment, ignoring point of view*

`distance { value: Number, unit: ['mm', 'cm', 'm', 'km'] }`

`duration { value: Number, unit: ['ms', 's', 'm', 'h'] }`

`speed { [angle, distance], duration }`

## Entities

`direction { angle }`

`precise-position { angle, distance }`

`circle { radius: distance }`

`reactangle { height: distance, width: distance }`

`2d-shape [circle, reactangle]`

`area { center: precise-position, shape: 2d-shape }`

`vague-position: area`

`position: [direction, precise-position, vague-position]`

`sphere { radius: distance }`

`block { height: distance, width: distance, depth: distance }`

`3d-shape [sphere, block]`

`shape: [2d-shape, 3d-shape]`

`something { position, shape }`

`item { activate: Function, deactivate: Function }`

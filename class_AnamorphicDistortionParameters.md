# unreal.AnamorphicDistortionParameters

```python
class unreal.AnamorphicDistortionParameters(pixel_aspect:float=0.0, cx02:float=0.0, cx04:float=0.0, cx22:float=0.0, cx24:float=0.0, cx44:float=0.0, cy02:float=0.0, cy04:float=0.0, cy22:float=0.0, cy24:float=0.0, cy44:float=0.0, squeeze_x:float=0.0, squeeze_y:float=0.0, lens_rotation:float=0.0)
```


**Bases:** ``StructBase``


Lens distortion parameters for the 3DE4 Anamorphic - Standard Degree 4 model
All parameters are unitless and represent the coefficients used to undistort a distorted image
For complete model description, see “tde4\_ldm\_standard.pdf” from https://www.3dequalizer.com/ in the Lens Distortion Plugin Kit v2.8

**C++ Source:**

- **Plugin**: CameraCalibrationCore

- **Module**: CameraCalibrationCore

- **File**: AnamorphicLensModel.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `cx02` (float): [Read-Write] X coefficient of the r^2 term

- `cx04` (float): [Read-Write] X coefficient of the r^4 term

- `cx22` (float): [Read-Write] X coefficient of the r^2\*cos(2\*phi) term

- `cx24` (float): [Read-Write] X coefficient of the r^4\*cos(2\*phi) term

- `cx44` (float): [Read-Write] X coefficient of the r^4\*cos(4\*phi) term

- `cy02` (float): [Read-Write] Y coefficient of the r^2 term

- `cy04` (float): [Read-Write] Y coefficient of the r^4 term

- `cy22` (float): [Read-Write] Y coefficient of the r^2\*cos(2\*phi) term

- `cy24` (float): [Read-Write] Y coefficient of the r^4\*cos(2\*phi) term

- `cy44` (float): [Read-Write] Y coefficient of the r^4\*cos(4\*phi) term

- `lens_rotation` (float): [Read-Write] Lens Rotation in degrees. Represents mounting inaccuracies (should be small, between -2 and +2 degrees)

- `pixel_aspect` (float): [Read-Write] Anamorphic Squeeze (the ratio of the filmback size to the size of the rasterized image)

- `squeeze_x` (float): [Read-Write] Squeeze Factor (should be small, relatively close to 1.0)

- `squeeze_y` (float): [Read-Write] Squeeze Factor (should be small, relatively close to 1.0)



---

_property_ `cx02`: float

[Read-Write] X coefficient of the r^2 term

**Type:**

( float)


---

_property_ `cx04`: float

[Read-Write] X coefficient of the r^4 term

**Type:**

( float)


---

_property_ `cx22`: float

[Read-Write] X coefficient of the r^2\*cos(2\*phi) term

**Type:**

( float)


---

_property_ `cx24`: float

[Read-Write] X coefficient of the r^4\*cos(2\*phi) term

**Type:**

( float)


---

_property_ `cx44`: float

[Read-Write] X coefficient of the r^4\*cos(4\*phi) term

**Type:**

( float)


---

_property_ `cy02`: float

[Read-Write] Y coefficient of the r^2 term

**Type:**

( float)


---

_property_ `cy04`: float

[Read-Write] Y coefficient of the r^4 term

**Type:**

( float)


---

_property_ `cy22`: float

[Read-Write] Y coefficient of the r^2\*cos(2\*phi) term

**Type:**

( float)


---

_property_ `cy24`: float

[Read-Write] Y coefficient of the r^4\*cos(2\*phi) term

**Type:**

( float)


---

_property_ `cy44`: float

[Read-Write] Y coefficient of the r^4\*cos(4\*phi) term

**Type:**

( float)


---

_property_ `lens_rotation`: float

[Read-Write] Lens Rotation in degrees. Represents mounting inaccuracies (should be small, between -2 and +2 degrees)

**Type:**

( float)


---

_property_ `pixel_aspect`: float

[Read-Write] Anamorphic Squeeze (the ratio of the filmback size to the size of the rasterized image)

**Type:**

( float)


---

_property_ `squeeze_x`: float

[Read-Write] Squeeze Factor (should be small, relatively close to 1.0)

**Type:**

( float)


---

_property_ `squeeze_y`: float

[Read-Write] Squeeze Factor (should be small, relatively close to 1.0)

**Type:**

( float)

### Table of Contents

- `unreal.AnamorphicDistortionParameters`
  - `AnamorphicDistortionParameters`
    - `AnamorphicDistortionParameters.cx02`
    - `AnamorphicDistortionParameters.cx04`
    - `AnamorphicDistortionParameters.cx22`
    - `AnamorphicDistortionParameters.cx24`
    - `AnamorphicDistortionParameters.cx44`
    - `AnamorphicDistortionParameters.cy02`
    - `AnamorphicDistortionParameters.cy04`
    - `AnamorphicDistortionParameters.cy22`
    - `AnamorphicDistortionParameters.cy24`
    - `AnamorphicDistortionParameters.cy44`
    - `AnamorphicDistortionParameters.lens_rotation`
    - `AnamorphicDistortionParameters.pixel_aspect`
    - `AnamorphicDistortionParameters.squeeze_x`
    - `AnamorphicDistortionParameters.squeeze_y`
# unreal.SphericalDistortionParameters

```python
class unreal.SphericalDistortionParameters(k1:float=0.0, k2:float=0.0, k3:float=0.0, p1:float=0.0, p2:float=0.0)
```


**Bases:** ``StructBase``


Spherical lens distortion parameters
All parameters are unitless and represent the coefficients used to undistort a distorted image
Refer to the OpenCV camera calibration documentation for the intended units/usage of these parameters:
https://docs.opencv.org/3.4/d9/d0c/group\_\_calib3d.html

**C++ Source:**

- **Plugin**: CameraCalibrationCore

- **Module**: CameraCalibrationCore

- **File**: SphericalLensModel.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `k1` (float): [Read-Write] Radial coefficient of the r^2 term

- `k2` (float): [Read-Write] Radial coefficient of the r^4 term

- `k3` (float): [Read-Write] Radial coefficient of the r^6 term

- `p1` (float): [Read-Write] First tangential coefficient

- `p2` (float): [Read-Write] Second tangential coefficient



---

_property_ `k1`: float

[Read-Write] Radial coefficient of the r^2 term

**Type:**

( float)


---

_property_ `k2`: float

[Read-Write] Radial coefficient of the r^4 term

**Type:**

( float)


---

_property_ `k3`: float

[Read-Write] Radial coefficient of the r^6 term

**Type:**

( float)


---

_property_ `p1`: float

[Read-Write] First tangential coefficient

**Type:**

( float)


---

_property_ `p2`: float

[Read-Write] Second tangential coefficient

**Type:**

( float)

### Table of Contents

- `unreal.SphericalDistortionParameters`
  - `SphericalDistortionParameters`
    - `SphericalDistortionParameters.k1`
    - `SphericalDistortionParameters.k2`
    - `SphericalDistortionParameters.k3`
    - `SphericalDistortionParameters.p1`
    - `SphericalDistortionParameters.p2`
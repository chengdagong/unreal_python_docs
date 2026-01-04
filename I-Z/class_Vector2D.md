# unreal.Vector2D

```python
class unreal.Vector2D(x:float=0.0, y:float=0.0)
```


**Bases:** ``StructBase``


A vector in 2-D space composed of components (X, Y) with floating point precision.
note: The full C++ class is located here: EngineSourceRuntimeCorePublicMathVector2D.h

**C++ Source:**

- **Module**: CoreUObject

- **File**: NoExportTypes.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `x` (double): [Read-Write]

- `y` (double): [Read-Write]


ONE _: Vector2D_

2D one vector constant (1,1)

**Type:**

( Vector2D)

UNIT45\_DEG _: Vector2D_

//en.wikipedia.org/wiki/Unit\_vector

**Type:**

( Vector2D)

**Type:**

2D unit vector constant along the 45 degree angle or symmetrical positive axes (sqrt(.5),sqrt(.5)) or (.707,.707). https

ZERO _: Vector2D_

2D zero vector constant (0,0)

**Type:**

( Vector2D)


---

**__add__**( _other:Vector2D_) → `None`

**Overloads:**

- `Vector2D` Returns addition of Vector A and Vector B (A + B)

- `double` Returns Vector A added by B



---

**__eq__**( _other:object_) → `bool`

**Overloads:**

- `Vector2D` Returns true if vector A is equal to vector B (A == B)



---

**__iadd__**( _other:Vector2D_) → `None`

**Overloads:**

- `Vector2D` Returns addition of Vector A and Vector B (A + B)

- `double` Returns Vector A added by B



---

**__imul__**( _other:Vector2D_) → `None`

**Overloads:**

- `Vector2D` Element-wise Vector multiplication (Result = {A.x\*B.x, A.y\*B.y})

- `double` Returns Vector A scaled by B



---

**__isub__**( _other:Vector2D_) → `None`

**Overloads:**

- `Vector2D` Returns subtraction of Vector B from Vector A (A - B)

- `double` Returns Vector A subtracted by B



---

**__mul__**( _other:Vector2D_) → `None`

**Overloads:**

- `Vector2D` Element-wise Vector multiplication (Result = {A.x\*B.x, A.y\*B.y})

- `double` Returns Vector A scaled by B



---

**__ne__**( _other:object_) → `bool`

**Overloads:**

- `Vector2D` Returns true if vector2D A is not equal to vector2D B (A != B) within a specified error tolerance



---

**__neg__**() → `None`

Gets a negated copy of the vector.


---

**__or__**( _other:Vector2D_) → `None`

**Overloads:**

- `Vector2D` Returns the dot product of two 2d vectors - see http://mathworld.wolfram.com/DotProduct.html



---

**__sub__**( _other:Vector2D_) → `None`

**Overloads:**

- `Vector2D` Returns subtraction of Vector B from Vector A (A - B)

- `double` Returns Vector A subtracted by B



---

**__truediv__**( _other:Vector2D_) → `None`

**Overloads:**

- `Vector2D` Element-wise Vector divide (Result = {A.x/B.x, A.y/B.y})

- `double` Returns Vector A divided by B



---

**__xor__**( _other:Vector2D_) → `None`

**Overloads:**

- `Vector2D` Returns the cross product of two 2d vectors - see http://mathworld.wolfram.com/CrossProduct.html



---

**add**( _b_) → `Vector2D`

Returns addition of Vector A and Vector B (A + B)

Parameters:

**b** ( _Vector2D_)

Return type:

Vector2D


---

**add_float**( _b_) → `Vector2D`

Returns Vector A added by B

Parameters:

**b** ( _double_)

Return type:

Vector2D


---

**clamped_axes**( _min_axis_val_, _max_axis_val_) → `Vector2D`

Creates a copy of this vector with both axes clamped to the given range.

Parameters:

- **min\_axis\_val** ( _double_)

- **max\_axis\_val** ( _double_)


Returns:

New vector with clamped axes.

Return type:

Vector2D


---

**cross**( _b_) → `double`

Returns the cross product of two 2d vectors - see http://mathworld.wolfram.com/CrossProduct.html

Parameters:

**b** ( _Vector2D_)

Return type:

double


---

**distance**( _v2_) → `double`

Distance between two 2D points.

Parameters:

**v2** ( _Vector2D_) – The second point.

Returns:

The distance between two 2D points.

Return type:

double


---

**distance_squared**( _v2_) → `double`

Squared distance between two 2D points.

Parameters:

**v2** ( _Vector2D_) – The second point.

Returns:

The squared distance between two 2D points.

Return type:

double


---

**divide**( _b_) → `Vector2D`

Element-wise Vector divide (Result = {A.x/B.x, A.y/B.y})

Parameters:

**b** ( _Vector2D_)

Return type:

Vector2D


---

**divide_float**( _b=1.000000_) → `Vector2D`

Returns Vector A divided by B

Parameters:

**b** ( _double_)

Return type:

Vector2D


---

**dot**( _b_) → `double`

Returns the dot product of two 2d vectors - see http://mathworld.wolfram.com/DotProduct.html

Parameters:

**b** ( _Vector2D_)

Return type:

double


---

**equals**( _b_) → `bool`

Returns true if vector A is equal to vector B (A == B)

Parameters:

**b** ( _Vector2D_)

Return type:

bool


---

**get_abs**() → `Vector2D`

Get a copy of this vector with absolute value of each component.

Returns:

A copy of this vector with absolute value of each component.

Return type:

Vector2D


---

**get_abs_max**() → `double`

Get the maximum absolute value of the vector’s components.

Returns:

The maximum absolute value of the vector’s components.

Return type:

double


---

**get_max**() → `double`

Get the maximum value of the vector’s components.

Returns:

The maximum value of the vector’s components.

Return type:

double


---

**get_min**() → `double`

Get the minimum value of the vector’s components.

Returns:

The minimum value of the vector’s components.

Return type:

double


---

**get_rotated**( _angle_deg_) → `Vector2D`

Rotates around axis (0,0,1)

Parameters:

**angle\_deg** ( _float_) – Angle to rotate (in degrees)

Returns:

Rotated Vector

Return type:

Vector2D


---

**int_point**() → `IntPoint`

Converts a Vector2D to an IntPoint

Return type:

IntPoint


---

**interp_to**( _target_, _delta_time_, _interp_speed_) → `Vector2D`

Tries to reach Target based on distance from Current position, giving a nice smooth feeling when tracking a position.

Parameters:

- **target** ( _Vector2D_) – Target position

- **delta\_time** ( _float_) – Time since last tick

- **interp\_speed** ( _float_) – Interpolation speed, if the speed given is 0, then jump to the target.


Returns:

New interpolated position

Return type:

Vector2D


---

**interp_to_constant**( _target_, _delta_time_, _interp_speed_) → `Vector2D`

Tries to reach Target at a constant rate.

Parameters:

- **target** ( _Vector2D_) – Target position

- **delta\_time** ( _float_) – Time since last tick

- **interp\_speed** ( _float_) – Interpolation speed


Returns:

New interpolated position

Return type:

Vector2D


---

**is_near_equal**( _b_, _error_tolerance=0.000100_) → `bool`

Returns true if vector2D A is equal to vector2D B (A == B) within a specified error tolerance

Parameters:

- **b** ( _Vector2D_)

- **error\_tolerance** ( _float_)


Return type:

bool


---

**is_nearly_zero**( _tolerance=0.000100_) → `bool`

Checks whether vector is near to zero within a specified tolerance.

Parameters:

**tolerance** ( _float_) – Error tolerance.

Returns:

true if vector is in tolerance to zero, otherwise false.

Return type:

bool


---

**is_not_near_equal**( _b_, _error_tolerance=0.000100_) → `bool`

Returns true if vector2D A is not equal to vector2D B (A != B) within a specified error tolerance

Parameters:

- **b** ( _Vector2D_)

- **error\_tolerance** ( _float_)


Return type:

bool


---

**is_zero**() → `bool`

Checks whether all components of the vector are exactly zero.

Returns:

true if vector is exactly zero, otherwise false.

Return type:

bool


---

**length**() → `double`

Returns the length of a 2D Vector.

Return type:

double


---

**length_squared**() → `double`

Returns the squared length of a 2D Vector.

Return type:

double


---

**multiply**( _b_) → `Vector2D`

Element-wise Vector multiplication (Result = {A.x\*B.x, A.y\*B.y})

Parameters:

**b** ( _Vector2D_)

Return type:

Vector2D


---

**multiply_float**( _b_) → `Vector2D`

Returns Vector A scaled by B

Parameters:

**b** ( _double_)

Return type:

Vector2D


---

**negated**() → `Vector2D`

Gets a negated copy of the vector.

Return type:

Vector2D


---

**normal**( _tolerance=0.000000_) → `Vector2D`

Gets a normalized copy of the vector, checking it is safe to do so based on the length.
Returns zero vector if vector length is too small to safely normalize.

Parameters:

**tolerance** ( _float_) – Minimum squared length of vector for normalization.

Returns:

A normalized copy of the vector if safe, (0,0) otherwise.

Return type:

Vector2D


---

**normal_unsafe**() → `Vector2D`

Returns a unit normal version of the 2D vector

Return type:

Vector2D


---

**normalize**( _tolerance=0.000000_) → `None`

Normalize this vector in-place if it is large enough, set it to (0,0) otherwise.
see: NormalSafe2D()

Parameters:

**tolerance** ( _float_) – Minimum squared length of vector for normalization.


---

**not_equal**( _b_) → `bool`

Returns true if vector2D A is not equal to vector2D B (A != B) within a specified error tolerance

Parameters:

**b** ( _Vector2D_)

Return type:

bool


---

**set**( _x_, _y_) → `None`

Set the values of the vector directly.

Parameters:

- **x** ( _double_)

- **y** ( _double_)



---

**spherical_to_unit_cartesian**() → `Vector`

Converts spherical coordinates on the unit sphere into a Cartesian unit length vector.

Return type:

Vector


---

**subtract**( _b_) → `Vector2D`

Returns subtraction of Vector B from Vector A (A - B)

Parameters:

**b** ( _Vector2D_)

Return type:

Vector2D


---

**subtract_float**( _b_) → `Vector2D`

Returns Vector A subtracted by B

Parameters:

**b** ( _double_)

Return type:

Vector2D

to\_direction\_and\_length( _)->(out\_dir=Vector2D_, _out\_length=double_)

Util to convert this vector into a unit direction vector and its original length.

Returns:

out\_dir (Vector2D): Reference passed in to store unit direction vector.

out\_length (double): Reference passed in to store length of the vector.

Return type:

tuple


---

**to_rounded**() → `Vector2D`

Get this vector as a vector where each component has been rounded to the nearest int.

Returns:

New FVector2D from this vector that is rounded.

Return type:

Vector2D


---

**to_sign**() → `Vector2D`

Get a copy of the vector as sign only.
Each component is set to +1 or -1, with the sign of zero treated as +1.

Returns:

A copy of the vector with each component set to +1 or -1

Return type:

Vector2D


---

**truncated**() → `IntVector2`

Rounds A to an integer with truncation towards zero for each element in a vector2D. (e.g. -1.7 truncated to -1, 2.8 truncated to 2)

Return type:

IntVector2


---

**vector**( _z=0.000000_) → `Vector`

Converts a Vector2D to a Vector

Parameters:

**z** ( _float_)

Return type:

Vector


---

_property_ `x`: float

[Read-Write]

**Type:**

(double)


---

_property_ `y`: float

[Read-Write]

**Type:**

(double)

### Table of Contents

- `unreal.Vector2D`
  - `Vector2D`
    - `Vector2D.ONE`
    - `Vector2D.UNIT45_DEG`
    - `Vector2D.ZERO`
    - `Vector2D.__add__()`
    - `Vector2D.__eq__()`
    - `Vector2D.__iadd__()`
    - `Vector2D.__imul__()`
    - `Vector2D.__isub__()`
    - `Vector2D.__mul__()`
    - `Vector2D.__ne__()`
    - `Vector2D.__neg__()`
    - `Vector2D.__or__()`
    - `Vector2D.__sub__()`
    - `Vector2D.__truediv__()`
    - `Vector2D.__xor__()`
    - `Vector2D.add()`
    - `Vector2D.add_float()`
    - `Vector2D.clamped_axes()`
    - `Vector2D.cross()`
    - `Vector2D.distance()`
    - `Vector2D.distance_squared()`
    - `Vector2D.divide()`
    - `Vector2D.divide_float()`
    - `Vector2D.dot()`
    - `Vector2D.equals()`
    - `Vector2D.get_abs()`
    - `Vector2D.get_abs_max()`
    - `Vector2D.get_max()`
    - `Vector2D.get_min()`
    - `Vector2D.get_rotated()`
    - `Vector2D.int_point()`
    - `Vector2D.interp_to()`
    - `Vector2D.interp_to_constant()`
    - `Vector2D.is_near_equal()`
    - `Vector2D.is_nearly_zero()`
    - `Vector2D.is_not_near_equal()`
    - `Vector2D.is_zero()`
    - `Vector2D.length()`
    - `Vector2D.length_squared()`
    - `Vector2D.multiply()`
    - `Vector2D.multiply_float()`
    - `Vector2D.negated()`
    - `Vector2D.normal()`
    - `Vector2D.normal_unsafe()`
    - `Vector2D.normalize()`
    - `Vector2D.not_equal()`
    - `Vector2D.set()`
    - `Vector2D.spherical_to_unit_cartesian()`
    - `Vector2D.subtract()`
    - `Vector2D.subtract_float()`
    - `Vector2D.to_direction_and_length()`
    - `Vector2D.to_rounded()`
    - `Vector2D.to_sign()`
    - `Vector2D.truncated()`
    - `Vector2D.vector()`
    - `Vector2D.x`
    - `Vector2D.y`
# unreal.Vector

```python
class unreal.Vector(x:float=0.0, y:float=0.0, z:float=0.0)
```


**Bases:** ``StructBase``


A point or direction FVector in 3d space.
note: The full C++ class is located here: EngineSourceRuntimeCorePublicMathVector.h

**C++ Source:**

- **Module**: CoreUObject

- **File**: NoExportTypes.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `x` (double): [Read-Write]

- `y` (double): [Read-Write]

- `z` (double): [Read-Write]


BACKWARD _: Vector_

3D vector Unreal backward direction constant (-1,0,0)

**Type:**

( Vector)

DOWN _: Vector_

3D vector Unreal down direction constant (0,0,-1)

**Type:**

( Vector)

FORWARD _: Vector_

3D vector Unreal forward direction constant (1,0,0)

**Type:**

( Vector)

LEFT _: Vector_

3D vector Unreal left direction constant (0,-1,0)

**Type:**

( Vector)

ONE _: Vector_

3D vector one constant (1,1,1)

**Type:**

( Vector)

RIGHT _: Vector_

3D vector Unreal right direction constant (0,1,0)

**Type:**

( Vector)

UP _: Vector_

3D vector Unreal up direction constant (0,0,1)

**Type:**

( Vector)

ZERO _: Vector_

3D vector zero constant (0,0,0)

**Type:**

( Vector)


---

**__add__**( _other:Vector_) → `None`

**Overloads:**

- `Vector` Vector addition



---

**__eq__**( _other:object_) → `bool`

**Overloads:**

- `Vector` Returns true if vector A is equal to vector B (A == B)



---

**__iadd__**( _other:Vector_) → `None`

**Overloads:**

- `Vector` Vector addition



---

**__imul__**( _other:Vector_) → `None`

**Overloads:**

- `Vector` Element-wise Vector multiplication (Result = {A.x\*B.x, A.y\*B.y, A.z\*B.z})

- `double` Scales Vector A by B



---

**__isub__**( _other:Vector_) → `None`

**Overloads:**

- `Vector` Vector subtraction



---

**__mul__**( _other:Vector_) → `None`

**Overloads:**

- `Vector` Element-wise Vector multiplication (Result = {A.x\*B.x, A.y\*B.y, A.z\*B.z})

- `double` Scales Vector A by B



---

**__ne__**( _other:object_) → `bool`

**Overloads:**

- `Vector` Returns true if vector A is not equal to vector B (A != B)



---

**__neg__**() → `None`

Negate a vector.


---

**__or__**( _other:Vector_) → `None`

**Overloads:**

- `Vector` Returns the dot product of two 3d vectors - see http://mathworld.wolfram.com/DotProduct.html



---

**__sub__**( _other:Vector_) → `None`

**Overloads:**

- `Vector` Vector subtraction



---

**__truediv__**( _other:Vector_) → `None`

**Overloads:**

- `Vector` Element-wise Vector division (Result = {A.x/B.x, A.y/B.y, A.z/B.z})

- `double` Vector divide by a float



---

**__xor__**( _other:Vector_) → `None`

**Overloads:**

- `Vector` Returns the cross product of two 3d vectors - see http://mathworld.wolfram.com/CrossProduct.html



---

**add**( _b_) → `Vector`

Vector addition

Parameters:

**b** ( _Vector_)

Return type:

Vector


---

**add_bounded**( _add_vect_, _radius_) → `None`

Add a vector to this and clamp the result to an axis aligned cube centered at the origin.

Parameters:

- **add\_vect** ( _Vector_) – Vector to add.

- **radius** ( _float_) – Half size of the cube.



---

**add_float**( _b_) → `Vector`

Adds a float to each component of a vector

Parameters:

**b** ( _double_)

Return type:

Vector


---

**add_int**( _b_) → `Vector`

Adds an integer to each component of a vector

Parameters:

**b** ( _int32_)

Return type:

Vector


---

**assign**( _vector_) → `None`

Assign the values of the supplied vector.

Parameters:

**vector** ( _Vector_) – Vector to copy values from.


---

**bounded_to_box**( _box_min_, _box_max_) → `Vector`

Get a copy of this vector, clamped inside of the specified axis aligned cube.

Parameters:

- **box\_min** ( _Vector_)

- **box\_max** ( _Vector_)


Return type:

Vector


---

**bounded_to_cube**( _radius_) → `Vector`

Get a copy of this vector, clamped inside of an axis aligned cube centered at the origin.

Parameters:

**radius** ( _float_) – Half size of the cube (or radius of sphere circumscribed in the cube).

Returns:

A copy of this vector, bound by cube.

Return type:

Vector


---

**clamped_size**( _min_, _max_) → `Vector`

Create a copy of this vector, with its magnitude/size/length clamped between Min and Max.

Parameters:

- **min** ( _double_)

- **max** ( _double_)


Return type:

Vector


---

**clamped_size2d**( _min_, _max_) → `Vector`

Create a copy of this vector, with the 2D magnitude/size/length clamped between Min and Max. Z is unchanged.

Parameters:

- **min** ( _double_)

- **max** ( _double_)


Return type:

Vector


---

**clamped_size_max**( _max_) → `Vector`

Create a copy of this vector, with its maximum magnitude/size/length clamped to MaxSize.

Parameters:

**max** ( _double_)

Return type:

Vector


---

**clamped_size_max2d**( _max_) → `Vector`

Create a copy of this vector, with the maximum 2D magnitude/size/length clamped to MaxSize. Z is unchanged.

Parameters:

**max** ( _double_)

Return type:

Vector


---

**cosine_angle2d**( _b_) → `double`

Returns the cosine of the angle between this vector and another projected onto the XY plane (no Z).

Parameters:

**b** ( _Vector_) – the other vector to find the 2D cosine of the angle with.

Returns:

The cosine.

Return type:

double


---

**cross**( _b_) → `Vector`

Returns the cross product of two 3d vectors - see http://mathworld.wolfram.com/CrossProduct.html

Parameters:

**b** ( _Vector_)

Return type:

Vector


---

**direction_unit_to**( _to_) → `Vector`

Find the unit direction vector from one position to another or (0,0,0) if positions are the same.

Parameters:

**to** ( _Vector_)

Return type:

Vector


---

**distance**( _v2_) → `double`

Distance between two points.

Parameters:

**v2** ( _Vector_) – The second point.

Returns:

The distance between two points.

Return type:

double


---

**distance2d**( _v2_) → `double`

Euclidean distance between two points in the XY plane (ignoring Z).

Parameters:

**v2** ( _Vector_) – The second point.

Returns:

The distance between two points in the XY plane.

Return type:

double


---

**distance2d_squared**( _v2_) → `double`

Squared euclidean distance between two points in the XY plane (ignoring Z).

Parameters:

**v2** ( _Vector_) – The second point.

Returns:

The distance between two points in the XY plane.

Return type:

double


---

**distance_squared**( _v2_) → `double`

Squared distance between two points.

Parameters:

**v2** ( _Vector_) – The second point.

Returns:

The squared distance between two points.

Return type:

double


---

**divide**( _b=[1.000000, 1.000000, 1.000000]_) → `Vector`

Element-wise Vector division (Result = {A.x/B.x, A.y/B.y, A.z/B.z})

Parameters:

**b** ( _Vector_)

Return type:

Vector


---

**divide_float**( _b=1.000000_) → `Vector`

Vector divide by a float

Parameters:

**b** ( _double_)

Return type:

Vector


---

**divide_int**( _b=1_) → `Vector`

Vector divide by an integer

Parameters:

**b** ( _int32_)

Return type:

Vector


---

**dot**( _b_) → `double`

Returns the dot product of two 3d vectors - see http://mathworld.wolfram.com/DotProduct.html

Parameters:

**b** ( _Vector_)

Return type:

double


---

**equals**( _b_) → `bool`

Returns true if vector A is equal to vector B (A == B)

Parameters:

**b** ( _Vector_)

Return type:

bool


---

**find_quat_between_normals**( _end_normal_) → `Quat`

Generates the ‘smallest’ (geodesic) rotation around a sphere between two normals (assumed to be unit length).

Parameters:

**end\_normal** ( _Vector_)

Returns:

Quat that will rotate from Start to End

Return type:

Quat


---

**find_quat_between_vectors**( _end_) → `Quat`

Generates the ‘smallest’ (geodesic) rotation around a sphere between two vectors of arbitrary length.

Parameters:

**end** ( _Vector_) – Vector the rotation ends at

Returns:

Quat that will rotate from Start to End

Return type:

Quat


---

**get_abs**() → `Vector`

Get a copy of this vector with absolute value of each component.

Returns:

A copy of this vector with absolute value of each component.

Return type:

Vector


---

**get_abs_max**() → `double`

Find the maximum absolute element (abs(X), abs(Y) or abs(Z)) of a vector

Return type:

double


---

**get_abs_min**() → `double`

Find the minimum absolute element (abs(X), abs(Y) or abs(Z)) of a vector

Return type:

double


---

**get_max**( _b_) → `Vector`

Find the maximum elements (X, Y and Z) between the two vector’s components

Parameters:

**b** ( _Vector_)

Return type:

Vector


---

**get_max_element**() → `double`

Find the maximum element (X, Y or Z) of a vector

Return type:

double


---

**get_min**( _b_) → `Vector`

Find the minimum elements (X, Y and Z) between the two vector’s components

Parameters:

**b** ( _Vector_)

Return type:

Vector


---

**get_min_element**() → `double`

Find the minimum element (X, Y or Z) of a vector

Return type:

double


---

**get_projection**() → `Vector`

Projects 2D components of vector based on Z.

Returns:

Projected version of vector based on Z.

Return type:

Vector


---

**get_sign_vector**() → `Vector`

Get a copy of the vector as sign only.
Each component is set to +1 or -1, with the sign of zero treated as +1.

Return type:

Vector


---

**heading_angle**() → `double`

Convert a direction vector into a ‘heading’ angle.

Returns:

‘Heading’ angle between +/-PI radians. 0 is pointing down +X.

Return type:

double

interp\_spring\_to( _target,spring\_state,stiffness,critical\_damping\_factor,delta\_time,mass=1.000000,target\_velocity\_amount=1.000000,clamp=False,min\_value=[-1.000000,-1.000000,-1.000000],max\_value=[1.000000,1.000000,1.000000],initialize\_from\_target=False)->(Vector,spring\_state=VectorSpringState_)

Uses a simple spring model to interpolate a vector from Current to Target.

Parameters:

- **target** ( _Vector_) – Target value

- **spring\_state** ( _VectorSpringState_) – Data related to spring model (velocity, error, etc..) - Create a unique variable per spring

- **stiffness** ( _float_) – How stiff the spring model is (more stiffness means more oscillation around the target value)

- **critical\_damping\_factor** ( _float_) – How much damping to apply to the spring (0 means no damping, 1 means critically damped which means no oscillation)

- **delta\_time** ( _float_) – Time difference since the last update

- **mass** ( _float_) – Multiplier that acts like mass on a spring

- **target\_velocity\_amount** ( _float_) – If 1 then the target velocity will be calculated and used, which results following the target more closely/without lag. Values down to zero (recommended when using this to smooth data) will progressively disable this effect.

- **clamp** ( _bool_) – Whether to use the Min/Max values to clamp the motion

- **min\_value** ( _Vector_) – Clamps the minimum output value and cancels the velocity if it reaches this limit

- **max\_value** ( _Vector_) – Clamps the maximum output value and cancels the velocity if it reaches this limit

- **initialize\_from\_target** ( _bool_) – If set then the current value will be set from the target on the first update


Returns:

spring\_state (VectorSpringState): Data related to spring model (velocity, error, etc..) - Create a unique variable per spring

Return type:

VectorSpringState


---

**interp_to**( _target_, _delta_time_, _interp_speed_) → `Vector`

Tries to reach Target based on distance from Current position, giving a nice smooth feeling when tracking a position.

Parameters:

- **target** ( _Vector_) – Target position

- **delta\_time** ( _float_) – Time since last tick

- **interp\_speed** ( _float_) – Interpolation speed, if the speed given is 0, then jump to the target.


Returns:

New interpolated position

Return type:

Vector


---

**interp_to_constant**( _target_, _delta_time_, _interp_speed_) → `Vector`

Tries to reach Target at a constant rate.

Parameters:

- **target** ( _Vector_) – Target position

- **delta\_time** ( _float_) – Time since last tick

- **interp\_speed** ( _float_) – Interpolation speed


Returns:

New interpolated position

Return type:

Vector


---

**is_nan**() → `bool`

Determines if any component is not a number (NAN)

Returns:

true if one or more components is NAN, otherwise false.

Return type:

bool


---

**is_near_equal**( _b_, _error_tolerance=0.000100_) → `bool`

Returns true if vector A is equal to vector B (A == B) within a specified error tolerance

Parameters:

- **b** ( _Vector_)

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

**is_normal**() → `bool`

Determines if vector is normalized / unit (length 1).

Returns:

true if normalized, false otherwise.

Return type:

bool


---

**is_not_near_equal**( _b_, _error_tolerance=0.000100_) → `bool`

Returns true if vector A is not equal to vector B (A != B) within a specified error tolerance

Parameters:

- **b** ( _Vector_)

- **error\_tolerance** ( _float_)


Return type:

bool


---

**is_uniform**( _tolerance=0.000100_) → `bool`

Checks whether all components of this vector are the same, within a tolerance.

Parameters:

**tolerance** ( _float_) – Error tolerance.

Returns:

true if the vectors are equal within tolerance limits, false otherwise.

Return type:

bool


---

**is_unit**( _squared_lenth_tolerance=0.000100_) → `bool`

Determines if vector is normalized / unit (length 1) within specified squared tolerance.

Parameters:

**squared\_lenth\_tolerance** ( _float_)

Returns:

true if unit, false otherwise.

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

Returns the length of the vector

Return type:

double


---

**length2d**() → `double`

Returns the length of the vector’s XY components.

Return type:

double


---

**length2d_squared**() → `double`

Returns the squared length of the vector’s XY components.

Return type:

double


---

**length_squared**() → `double`

Returns the squared length of the vector

Return type:

double


---

**lerp_to**( _b_, _alpha_) → `Vector`

Linearly interpolates between A and B based on Alpha (100% of A when Alpha=0 and 100% of B when Alpha=1)

Parameters:

- **b** ( _Vector_)

- **alpha** ( _float_)


Return type:

Vector


---

**linear_color**() → `LinearColor`

Converts a vector to LinearColor

Return type:

LinearColor


---

**make_from_rotation_vector**() → `Quat`

Constructs a quaternion corresponding to the rotation vector.
The direction of the vector represents the rotation axis,
and the magnitude the angle in degrees.

Return type:

Quat


---

**mirror_by_plane**( _plane_) → `Vector`

Mirrors a vector about a plane.

Parameters:

**plane** ( _Plane_)

Returns:

Mirrored vector.

Return type:

Vector


---

**mirror_by_vector**( _surface_normal_) → `Vector`

Given a direction vector and a surface normal, returns the vector reflected across the surface normal.
Produces a result like shining a laser at a mirror!

Parameters:

**surface\_normal** ( _Vector_) – A normal of the surface the ray should be reflected on.

Returns:

Reflected vector.

Return type:

Vector


---

**multiply**( _b_) → `Vector`

Element-wise Vector multiplication (Result = {A.x\*B.x, A.y\*B.y, A.z\*B.z})

Parameters:

**b** ( _Vector_)

Return type:

Vector


---

**multiply_float**( _b_) → `Vector`

Scales Vector A by B

Parameters:

**b** ( _double_)

Return type:

Vector


---

**multiply_int**( _b_) → `Vector`

Scales Vector A by B

Parameters:

**b** ( _int32_)

Return type:

Vector


---

**negated**() → `Vector`

Negate a vector.

Return type:

Vector


---

**normal**( _tolerance=0.000100_) → `Vector`

Gets a normalized unit copy of the vector, ensuring it is safe to do so based on the length.
Returns zero vector if vector length is too small to safely normalize.

Parameters:

**tolerance** ( _float_) – Minimum squared vector length.

Returns:

A normalized copy if safe, (0,0,0) otherwise.

Return type:

Vector


---

**normal2d**( _tolerance=0.000100_) → `Vector`

Gets a normalized unit copy of the 2D components of the vector, ensuring it is safe to do so. Z is set to zero.
Returns zero vector if vector length is too small to normalize.

Parameters:

**tolerance** ( _float_) – Minimum squared vector length.

Returns:

Normalized copy if safe, (0,0,0) otherwise.

Return type:

Vector


---

**normal_unsafe**() → `Vector`

Calculates normalized unit version of vector without checking for zero length.

Returns:

Normalized version of vector.

Return type:

Vector


---

**normalize**( _tolerance=0.000000_) → `None`

Normalize this vector in-place if it is large enough or set it to (0,0,0) otherwise.

Parameters:

**tolerance** ( _float_) – Minimum squared length of vector for normalization.


---

**not_equal**( _b_) → `bool`

Returns true if vector A is not equal to vector B (A != B)

Parameters:

**b** ( _Vector_)

Return type:

bool


---

**project_on_to**( _target_) → `Vector`

Projects one vector (V) onto another (Target) and returns the projected vector.
If Target is nearly zero in length, returns the zero vector.

Parameters:

**target** ( _Vector_) – Vector on which we are projecting.

Returns:

V projected on to Target.

Return type:

Vector


---

**project_on_to_normal**( _normal_) → `Vector`

Gets a copy of this vector projected onto the input vector, which is assumed to be unit length.

Parameters:

**normal** ( _Vector_) – Vector to project onto (assumed to be unit length).

Returns:

Projected vector.

Return type:

Vector


---

**project_on_to_plane**( _plane_normal_) → `Vector`

Projects a vector onto a plane defined by a normalized vector (PlaneNormal).

Parameters:

**plane\_normal** ( _Vector_) – Normal of the plane.

Returns:

Vector projected onto the plane.

Return type:

Vector


---

**project_point_on_to_plane**( _plane_base_, _plane_normal_) → `Vector`

Projects/snaps a point onto a plane defined by a point on the plane and a plane normal.

Parameters:

- **plane\_base** ( _Vector_) – A point on the plane.

- **plane\_normal** ( _Vector_) – Normal of the plane.


Returns:

Point projected onto the plane.

Return type:

Vector


---

**quaternion**() → `Quat`

Return the Quaternion orientation corresponding to the direction in which the vector points.
Similar to the FRotator version, returns a result without roll such that it preserves the up vector.
note: If you don’t care about preserving the up vector and just want the most direct rotation, you can use the faster ‘FindBetweenVectors(ForwardVector, YourVector)’ or ‘FindBetweenNormals(…)’ if you know the vector is of unit length.

Returns:

Quaternion from the Vector’s direction, without any roll.

Return type:

Quat


---

**random_point_in_box_extents**( _half_size_) → `Vector`

Returns a random point within the specified bounding box using the first vector as an origin and the second as the box extents.

Parameters:

**half\_size** ( _Vector_)

Return type:

Vector


---

**reciprocal**() → `Vector`

Gets the reciprocal of this vector, avoiding division by zero.
Zero components are set to BIG\_NUMBER.

Returns:

Reciprocal of this vector.

Return type:

Vector


---

**rotate**( _b_) → `Vector`

Returns result of vector A rotated by Rotator B

Parameters:

**b** ( _Rotator_)

Return type:

Vector


---

**rotate_angle_axis**( _angle_deg_, _axis_) → `Vector`

Returns result of vector A rotated by AngleDeg around Axis

Parameters:

- **angle\_deg** ( _float_)

- **axis** ( _Vector_)


Return type:

Vector


---

**rotator**() → `Rotator`

Return the FRotator orientation corresponding to the direction in which the vector points.
Sets Yaw and Pitch to the proper numbers, and sets Roll to zero because the roll can’t be determined from a vector.

Returns:

FRotator from the Vector’s direction, without any roll.

Return type:

Rotator


---

**rotator_from_axis_and_angle**( _angle_) → `Rotator`

Create a rotation from an axis and supplied angle (in degrees)

Parameters:

**angle** ( _float_)

Return type:

Rotator


---

**set**( _x_, _y_, _z_) → `None`

Set the values of the vector directly.

Parameters:

- **x** ( _double_)

- **y** ( _double_)

- **z** ( _double_)



---

**slerp_normals**( _normal_b_, _alpha_) → `Vector`

Interpolate from normalized vector A to normalized vector B along a spherical path.

Parameters:

- **normal\_b** ( _Vector_) – End target direction of interpolation, must be normalized.

- **alpha** ( _double_) – interpolation amount, usually between 0-1


Returns:

Vector after interpolating between A and B along a spherical path.

Return type:

Vector


---

**slerp_vectors**( _direction_, _alpha_) → `Vector`

Interpolate from a vector to the direction of another vector along a spherical path.

Parameters:

- **direction** ( _Vector_) – Target direction we interpolate to

- **alpha** ( _double_) – interpolation amount, usually between 0-1


Returns:

Vector after interpolating between Vector and Direction along a spherical path. The magnitude will remain the length of the starting vector.

Return type:

Vector


---

**snapped_to_grid**( _grid_size_) → `Vector`

Gets a copy of this vector snapped to a grid.

Parameters:

**grid\_size** ( _float_) – Grid dimension / step.

Returns:

A copy of this vector snapped to a grid.

Return type:

Vector


---

**subtract**( _b_) → `Vector`

Vector subtraction

Parameters:

**b** ( _Vector_)

Return type:

Vector


---

**subtract_float**( _b_) → `Vector`

Subtracts a float from each component of a vector

Parameters:

**b** ( _double_)

Return type:

Vector


---

**subtract_int**( _b_) → `Vector`

Subtracts an integer from each component of a vector

Parameters:

**b** ( _int32_)

Return type:

Vector


---

**to_degrees**() → `Vector`

Converts a vector containing radian values to a vector containing degree values.

Returns:

Vector containing degree values

Return type:

Vector


---

**to_radians**() → `Vector`

Converts a vector containing degree values to a vector containing radian values.

Returns:

Vector containing radian values

Return type:

Vector


---

**transform**() → `Transform`

Converts a vector to a transform. Uses vector as location

Return type:

Transform


---

**truncated**() → `IntVector`

Rounds A to an integer with truncation towards zero for each element in a vector. (e.g. -1.7 truncated to -1, 2.8 truncated to 2)

Return type:

IntVector


---

**unit_cartesian_to_spherical**() → `Vector2D`

Converts a Cartesian unit vector into spherical coordinates on the unit sphere.

Returns:

Output Theta will be in the range [0, PI], and output Phi will be in the range [-PI, PI].

Return type:

Vector2D


---

**unrotate**( _b_) → `Vector`

Returns result of vector A rotated by the inverse of Rotator B

Parameters:

**b** ( _Rotator_)

Return type:

Vector


---

**unwind_euler**() → `None`

When this vector contains Euler angles (degrees), ensure that angles are between +/-180


---

**vector2d**() → `Vector2D`

Converts a Vector to a Vector2D using the Vector’s (X, Y) coordinates

Return type:

Vector2D


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


---

_property_ `z`: float

[Read-Write]

**Type:**

(double)

### Table of Contents

- `unreal.Vector`
  - `Vector`
    - `Vector.BACKWARD`
    - `Vector.DOWN`
    - `Vector.FORWARD`
    - `Vector.LEFT`
    - `Vector.ONE`
    - `Vector.RIGHT`
    - `Vector.UP`
    - `Vector.ZERO`
    - `Vector.__add__()`
    - `Vector.__eq__()`
    - `Vector.__iadd__()`
    - `Vector.__imul__()`
    - `Vector.__isub__()`
    - `Vector.__mul__()`
    - `Vector.__ne__()`
    - `Vector.__neg__()`
    - `Vector.__or__()`
    - `Vector.__sub__()`
    - `Vector.__truediv__()`
    - `Vector.__xor__()`
    - `Vector.add()`
    - `Vector.add_bounded()`
    - `Vector.add_float()`
    - `Vector.add_int()`
    - `Vector.assign()`
    - `Vector.bounded_to_box()`
    - `Vector.bounded_to_cube()`
    - `Vector.clamped_size()`
    - `Vector.clamped_size2d()`
    - `Vector.clamped_size_max()`
    - `Vector.clamped_size_max2d()`
    - `Vector.cosine_angle2d()`
    - `Vector.cross()`
    - `Vector.direction_unit_to()`
    - `Vector.distance()`
    - `Vector.distance2d()`
    - `Vector.distance2d_squared()`
    - `Vector.distance_squared()`
    - `Vector.divide()`
    - `Vector.divide_float()`
    - `Vector.divide_int()`
    - `Vector.dot()`
    - `Vector.equals()`
    - `Vector.find_quat_between_normals()`
    - `Vector.find_quat_between_vectors()`
    - `Vector.get_abs()`
    - `Vector.get_abs_max()`
    - `Vector.get_abs_min()`
    - `Vector.get_max()`
    - `Vector.get_max_element()`
    - `Vector.get_min()`
    - `Vector.get_min_element()`
    - `Vector.get_projection()`
    - `Vector.get_sign_vector()`
    - `Vector.heading_angle()`
    - `Vector.interp_spring_to()`
    - `Vector.interp_to()`
    - `Vector.interp_to_constant()`
    - `Vector.is_nan()`
    - `Vector.is_near_equal()`
    - `Vector.is_nearly_zero()`
    - `Vector.is_normal()`
    - `Vector.is_not_near_equal()`
    - `Vector.is_uniform()`
    - `Vector.is_unit()`
    - `Vector.is_zero()`
    - `Vector.length()`
    - `Vector.length2d()`
    - `Vector.length2d_squared()`
    - `Vector.length_squared()`
    - `Vector.lerp_to()`
    - `Vector.linear_color()`
    - `Vector.make_from_rotation_vector()`
    - `Vector.mirror_by_plane()`
    - `Vector.mirror_by_vector()`
    - `Vector.multiply()`
    - `Vector.multiply_float()`
    - `Vector.multiply_int()`
    - `Vector.negated()`
    - `Vector.normal()`
    - `Vector.normal2d()`
    - `Vector.normal_unsafe()`
    - `Vector.normalize()`
    - `Vector.not_equal()`
    - `Vector.project_on_to()`
    - `Vector.project_on_to_normal()`
    - `Vector.project_on_to_plane()`
    - `Vector.project_point_on_to_plane()`
    - `Vector.quaternion()`
    - `Vector.random_point_in_box_extents()`
    - `Vector.reciprocal()`
    - `Vector.rotate()`
    - `Vector.rotate_angle_axis()`
    - `Vector.rotator()`
    - `Vector.rotator_from_axis_and_angle()`
    - `Vector.set()`
    - `Vector.slerp_normals()`
    - `Vector.slerp_vectors()`
    - `Vector.snapped_to_grid()`
    - `Vector.subtract()`
    - `Vector.subtract_float()`
    - `Vector.subtract_int()`
    - `Vector.to_degrees()`
    - `Vector.to_radians()`
    - `Vector.transform()`
    - `Vector.truncated()`
    - `Vector.unit_cartesian_to_spherical()`
    - `Vector.unrotate()`
    - `Vector.unwind_euler()`
    - `Vector.vector2d()`
    - `Vector.x`
    - `Vector.y`
    - `Vector.z`
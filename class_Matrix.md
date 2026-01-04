# unreal.Matrix

```python
class unreal.Matrix(x\plane:Plane=Ellipsis, y\plane:Plane=Ellipsis, z\plane:Plane=Ellipsis, w\plane:Plane=Ellipsis)
```


**Bases:** ``StructBase``


A 4x4 matrix.
note: The full C++ class is located here: EngineSourceRuntimeCorePublicMathMatrix.h

**C++ Source:**

- **Module**: CoreUObject

- **File**: NoExportTypes.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `w_plane` (Plane): [Read-Write]

- `x_plane` (Plane): [Read-Write]

- `y_plane` (Plane): [Read-Write]

- `z_plane` (Plane): [Read-Write]


IDENTITY _: Matrix_

Identity matrix

**Type:**

( Matrix)


---

**__add__**( _other:Matrix_) → `None`

**Overloads:**

- `Matrix` Gets the result of adding a matrix to this.

@param Other The Matrix to add.
@return The result of addition.



---

**__eq__**( _other:object_) → `bool`

**Overloads:**

- `Matrix` Checks whether another Matrix is equal to this, within specified tolerance.

@param Other The other Matrix.
@param Tolerance Error Tolerance.
@return true if two Matrix are equal, within specified tolerance, otherwise false.



---

**__iadd__**( _other:Matrix_) → `None`

**Overloads:**

- `Matrix` Gets the result of adding a matrix to this.

@param Other The Matrix to add.
@return The result of addition.



---

**__imul__**( _other:Matrix_) → `None`

**Overloads:**

- `Matrix` Gets the result of multiplying a Matrix to this.

@param Other The matrix to multiply this by.
@return The result of multiplication.

- `double` Multiplies all values of the matrix by a float.
If your Matrix represents a Transform that you wish to scale you should use Apply Scale instead



---

**__mul__**( _other:Matrix_) → `None`

**Overloads:**

- `Matrix` Gets the result of multiplying a Matrix to this.

@param Other The matrix to multiply this by.
@return The result of multiplication.

- `double` Multiplies all values of the matrix by a float.
If your Matrix represents a Transform that you wish to scale you should use Apply Scale instead



---

**__ne__**( _other:object_) → `bool`

**Overloads:**

- `Matrix` Checks whether another Matrix is not equal to this, within specified tolerance.

@param Other The other Matrix.
@return true if two Matrix are not equal, within specified tolerance, otherwise false.



---

**add**( _b_) → `Matrix`

Gets the result of adding a matrix to this.

Parameters:

**b** ( _Matrix_)

Returns:

The result of addition.

Return type:

Matrix


---

**apply_scale**( _scale_) → `Matrix`

Apply Scale to this matrix
(Assumes Matrix represents a transform)

Parameters:

**scale** ( _float_)

Return type:

Matrix


---

**concatenate_translation**( _translation_) → `Matrix`

Returns a matrix with an additional translation concatenated.
(Assumes Matrix represents a transform)

Parameters:

**translation** ( _Vector_)

Return type:

Matrix


---

**contains_na_n**() → `bool`

Returns true if any element of this matrix is NaN

Return type:

bool


---

**equals**( _b_, _tolerance=0.000100_) → `bool`

Checks whether another Matrix is equal to this, within specified tolerance.

Parameters:

- **b** ( _Matrix_)

- **tolerance** ( _float_) – Error Tolerance.


Returns:

true if two Matrix are equal, within specified tolerance, otherwise false.

Return type:

bool


---

**get_column**( _column_) → `Vector`

get a column of this matrix

Parameters:

**column** ( _MatrixColumns_)

Returns:

vector of the column

Return type:

Vector


---

**get_determinant**() → `floatReturns:`

determinant of this matrix.

Return type:

float


---

**get_frustum_bottom_plane**() → `PlaneorNone`

Get the bottom plane of the Frustum of this matrix
(Assumes Matrix represents a View Projection Matrix)

Returns:

out\_plane (Plane): the bottom plane of the Frustum of this matrix

Return type:

Plane or None


---

**get_frustum_far_plane**() → `PlaneorNone`

Get the far plane of the Frustum of this matrix
(Assumes Matrix represents a View Projection Matrix)

Returns:

out\_plane (Plane): the far plane of the Frustum of this matrix

Return type:

Plane or None


---

**get_frustum_left_plane**() → `PlaneorNone`

Get the left plane of the Frustum of this matrix
(Assumes Matrix represents a View Projection Matrix)

Returns:

out\_plane (Plane): the left plane of the Frustum of this matrix

Return type:

Plane or None


---

**get_frustum_near_plane**() → `PlaneorNone`

Get the near plane of the Frustum of this matrix
(Assumes Matrix represents a View Projection Matrix)

Returns:

out\_plane (Plane): the near plane of the Frustum of this matrix

Return type:

Plane or None


---

**get_frustum_right_plane**() → `PlaneorNone`

Get the right plane of the Frustum of this matrix
(Assumes Matrix represents a View Projection Matrix)

Returns:

out\_plane (Plane): the right plane of the Frustum of this matrix

Return type:

Plane or None


---

**get_frustum_top_plane**() → `PlaneorNone`

Get the top plane of the Frustum of this matrix
(Assumes Matrix represents a View Projection Matrix)

Returns:

out\_plane (Plane): the top plane of the Frustum of this matrix

Return type:

Plane or None


---

**get_inverse**() → `Matrix`

Get the inverse of the Matrix. Handles nil matrices.

Return type:

Matrix


---

**get_matrix_without_scale**( _tolerance=0.000000_) → `Matrix`

Returns matrix after RemoveScaling with error Tolerance
(Assumes Matrix represents a transform)

Parameters:

**tolerance** ( _float_)

Return type:

Matrix


---

**get_maximum_axis_scale**() → `floatReturns:`

the maximum magnitude of any row of the matrix. (Assumes Matrix represents a transform)

Return type:

float


---

**get_origin**() → `Vector`

Get the origin of the co-ordinate system
(Assumes Matrix represents a transform)

Returns:

co-ordinate system origin

Return type:

Vector


---

**get_rot_determinant**() → `floatReturns:`

the determinant of rotation 3x3 matrix (Assumes Top Left 3x3 Submatrix represents a Rotation)

Return type:

float


---

**get_rotator**() → `Rotator`

Get the rotator representation of this matrix
(Assumes Matrix represents a transform)

Returns:

rotator representation of this matrix

Return type:

Rotator


---

**get_scale_vector**( _tolerance=0.000000_) → `Vector`

return a 3D scale vector calculated from this matrix (where each component is the magnitude of a row vector) with error Tolerance.
(Assumes Matrix represents a transform)

Parameters:

**tolerance** ( _float_)

Return type:

Vector

get\_scaled\_axes( _)->(x=Vector_, _y=Vector_, _z=Vector_)

get axes of this matrix scaled by the scale of the matrix
(Assumes Matrix represents a transform)

Returns:

x (Vector): axes returned to this param

y (Vector): axes returned to this param

z (Vector): axes returned to this param

Return type:

tuple


---

**get_scaled_axis**( _axis_) → `Vector`

get axis of this matrix scaled by the scale of the matrix
(Assumes Matrix represents a transform)

Parameters:

**axis** ( _AxisType_)

Returns:

vector of the axis

Return type:

Vector


---

**get_transpose_adjoint**() → `Matrix`

Get the Transose Adjoint of the Matrix.

Return type:

Matrix


---

**get_transposed**() → `Matrix`

Transpose.

Return type:

Matrix

get\_unit\_axes( _)->(x=Vector_, _y=Vector_, _z=Vector_)

get unit length axes of this matrix
(Assumes Matrix represents a transform)

Returns:

x (Vector): axes returned to this param

y (Vector): axes returned to this param

z (Vector): axes returned to this param

Return type:

tuple


---

**get_unit_axis**( _axis_) → `Vector`

get unit length axis of this matrix
(Assumes Matrix represents a transform)

Parameters:

**axis** ( _AxisType_)

Returns:

vector of the axis

Return type:

Vector


---

**inverse_transform_position**( _v_) → `Vector`

Inverts the matrix and then transforms V - correctly handles scaling in this matrix.
(Assumes Matrix represents a transform)

Parameters:

**v** ( _Vector_)

Return type:

Vector


---

**inverse_transform_vector**( _v_) → `Vector`

Transform a direction vector by the inverse of this matrix - will not take into account translation part.
If you want to transform a surface normal (or plane) and correctly account for non-uniform scaling you should use TransformByUsingAdjointT with adjoint of matrix inverse.
(Assumes Matrix represents a transform)

Parameters:

**v** ( _Vector_)

Return type:

Vector


---

**mirror**( _mirror_axis_, _flip_axis_) → `Matrix`

Utility for mirroring this transform across a certain plane, and flipping one of the axis as well.
(Assumes Matrix represents a transform)

Parameters:

- **mirror\_axis** ( _AxisType_)

- **flip\_axis** ( _AxisType_)


Return type:

Matrix


---

**multiply**( _b_) → `Matrix`

Gets the result of multiplying a Matrix to this.

Parameters:

**b** ( _Matrix_)

Returns:

The result of multiplication.

Return type:

Matrix


---

**multiply_float**( _b_) → `Matrix`

Multiplies all values of the matrix by a float.
If your Matrix represents a Transform that you wish to scale you should use Apply Scale instead

Parameters:

**b** ( _double_)

Return type:

Matrix


---

**not_equal**( _b_, _tolerance=0.000100_) → `bool`

Checks whether another Matrix is not equal to this, within specified tolerance.

Parameters:

- **b** ( _Matrix_)

- **tolerance** ( _float_)


Returns:

true if two Matrix are not equal, within specified tolerance, otherwise false.

Return type:

bool


---

**remove_scaling**( _tolerance=0.000000_) → `None`

Remove any scaling from this matrix (ie magnitude of each row is 1) with error Tolerance
(Assumes Matrix represents a transform)

Parameters:

**tolerance** ( _float_)


---

**remove_translation**() → `Matrix`

Remove any translation from this matrix
(Assumes Matrix represents a transform)

Return type:

Matrix


---

**rotator**() → `Rotator`

Converts a Matrix to a Rotator
(Assumes Matrix represents a transform)

Return type:

Rotator


---

**scale_translation**( _scale3d_) → `Matrix`

Scale the translation part of the matrix by the supplied vector.
(Assumes Matrix represents a transform)

Parameters:

**scale3d** ( _Vector_)

Return type:

Matrix


---

**set_axis**( _axis_, _axis_vector_) → `None`

set an axis of this matrix
(Assumes Matrix represents a transform)

Parameters:

- **axis** ( _AxisType_) – vector of the axis

- **axis\_vector** ( _Vector_)



---

**set_column**( _column_, _value_) → `None`

Matrix Set Column

Parameters:

- **column** ( _MatrixColumns_)

- **value** ( _Vector_)



---

**set_origin**( _new_origin_) → `None`

Set the origin of the coordinate system to the given vector
(Assumes Matrix represents a transform)

Parameters:

**new\_origin** ( _Vector_)


---

**to_quat**() → `Quat`

Transform a rotation matrix into a quaternion.
(Assumes Matrix represents a transform)
warning: rotation part will need to be unit length for this to be right!

Return type:

Quat


---

**transform**() → `Transform`

Converts a Matrix to a Transform
(Assumes Matrix represents a transform)

Return type:

Transform


---

**transform_position**( _v_) → `Vector4`

Transform a location - will take into account translation part of the FMatrix.
(Assumes Matrix represents a transform)

Parameters:

**v** ( _Vector_)

Return type:

Vector4


---

**transform_vector**( _v_) → `Vector4`

Transform a direction vector - will not take into account translation part of the FMatrix.
If you want to transform a surface normal (or plane) and correctly account for non-uniform scaling you should use TransformByUsingAdjointT.
(Assumes Matrix represents a transform)

Parameters:

**v** ( _Vector_)

Return type:

Vector4


---

**transform_vector4**( _v_) → `Vector4`

Transform a vector by the matrix.
(Assumes Matrix represents a transform)

Parameters:

**v** ( _Vector4_)

Return type:

Vector4


---

_property_ `w_plane`: Plane

[Read-Write]

**Type:**

( Plane)


---

_property_ `x_plane`: Plane

[Read-Write]

**Type:**

( Plane)


---

_property_ `y_plane`: Plane

[Read-Write]

**Type:**

( Plane)


---

_property_ `z_plane`: Plane

[Read-Write]

**Type:**

( Plane)

### Table of Contents

- `unreal.Matrix`
  - `Matrix`
    - `Matrix.IDENTITY`
    - `Matrix.__add__()`
    - `Matrix.__eq__()`
    - `Matrix.__iadd__()`
    - `Matrix.__imul__()`
    - `Matrix.__mul__()`
    - `Matrix.__ne__()`
    - `Matrix.add()`
    - `Matrix.apply_scale()`
    - `Matrix.concatenate_translation()`
    - `Matrix.contains_na_n()`
    - `Matrix.equals()`
    - `Matrix.get_column()`
    - `Matrix.get_determinant()`
    - `Matrix.get_frustum_bottom_plane()`
    - `Matrix.get_frustum_far_plane()`
    - `Matrix.get_frustum_left_plane()`
    - `Matrix.get_frustum_near_plane()`
    - `Matrix.get_frustum_right_plane()`
    - `Matrix.get_frustum_top_plane()`
    - `Matrix.get_inverse()`
    - `Matrix.get_matrix_without_scale()`
    - `Matrix.get_maximum_axis_scale()`
    - `Matrix.get_origin()`
    - `Matrix.get_rot_determinant()`
    - `Matrix.get_rotator()`
    - `Matrix.get_scale_vector()`
    - `Matrix.get_scaled_axes()`
    - `Matrix.get_scaled_axis()`
    - `Matrix.get_transpose_adjoint()`
    - `Matrix.get_transposed()`
    - `Matrix.get_unit_axes()`
    - `Matrix.get_unit_axis()`
    - `Matrix.inverse_transform_position()`
    - `Matrix.inverse_transform_vector()`
    - `Matrix.mirror()`
    - `Matrix.multiply()`
    - `Matrix.multiply_float()`
    - `Matrix.not_equal()`
    - `Matrix.remove_scaling()`
    - `Matrix.remove_translation()`
    - `Matrix.rotator()`
    - `Matrix.scale_translation()`
    - `Matrix.set_axis()`
    - `Matrix.set_column()`
    - `Matrix.set_origin()`
    - `Matrix.to_quat()`
    - `Matrix.transform()`
    - `Matrix.transform_position()`
    - `Matrix.transform_vector()`
    - `Matrix.transform_vector4()`
    - `Matrix.w_plane`
    - `Matrix.x_plane`
    - `Matrix.y_plane`
    - `Matrix.z_plane`
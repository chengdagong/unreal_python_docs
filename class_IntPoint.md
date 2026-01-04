# unreal.IntPoint

```python
class unreal.IntPoint(x:int=0, y:int=0)
```


**Bases:** ``StructBase``


Screen coordinates.
note: The full C++ class is located here: EngineSourceRuntimeCorePublicMathIntPoint.h

**C++ Source:**

- **Module**: CoreUObject

- **File**: NoExportTypes.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `x` (int32): [Read-Write]

- `y` (int32): [Read-Write]


DOWN _: IntPoint_

Down Int Point (0, 1)

**Type:**

( IntPoint)

LEFT _: IntPoint_

Left Int Point (-1, 0)

**Type:**

( IntPoint)

ONE _: IntPoint_

One Int Point (1, 1)

**Type:**

( IntPoint)

RIGHT _: IntPoint_

Right Int Point (1, 0)

**Type:**

( IntPoint)

UP _: IntPoint_

Up Int Point (0, -1)

**Type:**

( IntPoint)

ZERO _: IntPoint_

Zero Int Point (0, 0)

**Type:**

( IntPoint)


---

**__add__**( _other:IntPoint_) → `None`

**Overloads:**

- `IntPoint` Returns IntPoint A added by B

- `int32` Addition (A - B)



---

**__eq__**( _other:object_) → `bool`

**Overloads:**

- `IntPoint` Returns true if IntPoint A is equal to IntPoint B (A == B)



---

**__iadd__**( _other:IntPoint_) → `None`

**Overloads:**

- `IntPoint` Returns IntPoint A added by B

- `int32` Addition (A - B)



---

**__imul__**( _other:IntPoint_) → `None`

**Overloads:**

- `IntPoint` Returns IntPoint A multiplied by B

- `int32` Multiplication (A \* B)



---

**__isub__**( _other:IntPoint_) → `None`

**Overloads:**

- `IntPoint` Returns IntPoint A subtracted by B

- `int32` Subtraction (A - B)



---

**__mul__**( _other:IntPoint_) → `None`

**Overloads:**

- `IntPoint` Returns IntPoint A multiplied by B

- `int32` Multiplication (A \* B)



---

**__ne__**( _other:object_) → `bool`

**Overloads:**

- `IntPoint` Returns true if IntPoint A is NOT equal to IntPoint B (A != B)



---

**__sub__**( _other:IntPoint_) → `None`

**Overloads:**

- `IntPoint` Returns IntPoint A subtracted by B

- `int32` Subtraction (A - B)



---

**__truediv__**( _other:IntPoint_) → `None`

**Overloads:**

- `IntPoint` Returns IntPoint A divided by B

- `int32` Division (A \* B)



---

**add**( _b_) → `IntPoint`

Returns IntPoint A added by B

Parameters:

**b** ( _IntPoint_)

Return type:

IntPoint


---

**add_int**( _b_) → `IntPoint`

Addition (A - B)

Parameters:

**b** ( _int32_)

Return type:

IntPoint


---

**divide**( _b_) → `IntPoint`

Returns IntPoint A divided by B

Parameters:

**b** ( _IntPoint_)

Return type:

IntPoint


---

**divide_int**( _b_) → `IntPoint`

Division (A \* B)

Parameters:

**b** ( _int32_)

Return type:

IntPoint


---

**equals**( _b_) → `bool`

Returns true if IntPoint A is equal to IntPoint B (A == B)

Parameters:

**b** ( _IntPoint_)

Return type:

bool


---

**multiply**( _b_) → `IntPoint`

Returns IntPoint A multiplied by B

Parameters:

**b** ( _IntPoint_)

Return type:

IntPoint


---

**multiply_int**( _b_) → `IntPoint`

Multiplication (A \* B)

Parameters:

**b** ( _int32_)

Return type:

IntPoint


---

**not_equal**( _b_) → `bool`

Returns true if IntPoint A is NOT equal to IntPoint B (A != B)

Parameters:

**b** ( _IntPoint_)

Return type:

bool


---

**subtract**( _b_) → `IntPoint`

Returns IntPoint A subtracted by B

Parameters:

**b** ( _IntPoint_)

Return type:

IntPoint


---

**subtract_int**( _b_) → `IntPoint`

Subtraction (A - B)

Parameters:

**b** ( _int32_)

Return type:

IntPoint


---

**vector2d**() → `Vector2D`

Converts an IntPoint to a Vector2D

Return type:

Vector2D


---

_property_ `x`: int

[Read-Write]

**Type:**

(int32)


---

_property_ `y`: int

[Read-Write]

**Type:**

(int32)

### Table of Contents

- `unreal.IntPoint`
  - `IntPoint`
    - `IntPoint.DOWN`
    - `IntPoint.LEFT`
    - `IntPoint.ONE`
    - `IntPoint.RIGHT`
    - `IntPoint.UP`
    - `IntPoint.ZERO`
    - `IntPoint.__add__()`
    - `IntPoint.__eq__()`
    - `IntPoint.__iadd__()`
    - `IntPoint.__imul__()`
    - `IntPoint.__isub__()`
    - `IntPoint.__mul__()`
    - `IntPoint.__ne__()`
    - `IntPoint.__sub__()`
    - `IntPoint.__truediv__()`
    - `IntPoint.add()`
    - `IntPoint.add_int()`
    - `IntPoint.divide()`
    - `IntPoint.divide_int()`
    - `IntPoint.equals()`
    - `IntPoint.multiply()`
    - `IntPoint.multiply_int()`
    - `IntPoint.not_equal()`
    - `IntPoint.subtract()`
    - `IntPoint.subtract_int()`
    - `IntPoint.vector2d()`
    - `IntPoint.x`
    - `IntPoint.y`
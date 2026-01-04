# unreal.AnimNode_CurveSource

```python
class unreal.AnimNode_CurveSource(source_pose:PoseLink=\[\], source_binding:Name='None', alpha:float=0.0)
```


**Bases:** ``AnimNode_Base``


Supply curves from some external source (e.g. audio)

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_CurveSource.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] How much we wan to blend the curve in by

- `source_binding` (Name): [Read-Write] The binding of the curve source we want to bind to.
We will bind to an object that implements ICurveSourceInterface. First we check
the actor that owns this (if any), then we check each of its components to see if we should
bind to the source that matches this name.

- `source_pose` (PoseLink): [Read-Write]



---

_property_ `alpha`: float

[Read-Write] How much we wan to blend the curve in by

**Type:**

( float)


---

_property_ `source_binding`: Name

[Read-Write] The binding of the curve source we want to bind to.
We will bind to an object that implements ICurveSourceInterface. First we check
the actor that owns this (if any), then we check each of its components to see if we should
bind to the source that matches this name.

**Type:**

( Name)


---

_property_ `source_pose`: PoseLink

[Read-Write]

**Type:**

( PoseLink)

### Table of Contents

- `unreal.AnimNode_CurveSource`
  - `AnimNode_CurveSource`
    - `AnimNode_CurveSource.alpha`
    - `AnimNode_CurveSource.source_binding`
    - `AnimNode_CurveSource.source_pose`
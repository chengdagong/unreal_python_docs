# unreal.MaterialDomain

```python
class unreal.MaterialDomain
```


**Bases:** ``EnumBase``


Defines the domain of a material.

**C++ Source:**

- **Module**: Engine

- **File**: MaterialDomain.h


MD\_DEFERRED\_DECAL _: MaterialDomain_ _=Ellipsis_

The material’s attributes describe a deferred decal, and will be mapped onto the decal’s frustum.

**Type:**

1

MD\_LIGHT\_FUNCTION _: MaterialDomain_ _=Ellipsis_

The material’s attributes describe a light’s distribution.

**Type:**

2

MD\_POST\_PROCESS _: MaterialDomain_ _=Ellipsis_

The material will be used in a custom post process pass.

**Type:**

4

MD\_SURFACE _: MaterialDomain_ _=Ellipsis_

The material’s attributes describe a 3d surface.

**Type:**

0

MD\_UI _: MaterialDomain_ _=Ellipsis_

The material will be used for UMG or Slate UI

**Type:**

5

MD\_VOLUME _: MaterialDomain_ _=Ellipsis_

The material’s attributes describe a 3d volume.

**Type:**

3

### Table of Contents

- `unreal.MaterialDomain`
  - `MaterialDomain`
    - `MaterialDomain.MD_DEFERRED_DECAL`
    - `MaterialDomain.MD_LIGHT_FUNCTION`
    - `MaterialDomain.MD_POST_PROCESS`
    - `MaterialDomain.MD_SURFACE`
    - `MaterialDomain.MD_UI`
    - `MaterialDomain.MD_VOLUME`
# unreal.GameplayCameraComponentActivationMode

```python
class unreal.GameplayCameraComponentActivationMode
```


**Bases:** ``EnumBase``


Defines how to activate a gameplay camera component.

**C++ Source:**

- **Plugin**: GameplayCameras

- **Module**: GameplayCameras

- **File**: GameplayCameraComponentBase.h


INSERT\_OR\_PUSH _: GameplayCameraComponentActivationMode_ _=Ellipsis_

Inserts the camera director as a child of the active one, or push it if there is no active one.

**Type:**

2

PUSH _: GameplayCameraComponentActivationMode_ _=Ellipsis_

Push the camera director over any existing ones.

**Type:**

0

PUSH\_AND\_INSERT _: GameplayCameraComponentActivationMode_ _=Ellipsis_

Push the camera director and try to insert any active one as a child.

**Type:**

1

### Table of Contents

- `unreal.GameplayCameraComponentActivationMode`
  - `GameplayCameraComponentActivationMode`
    - `GameplayCameraComponentActivationMode.INSERT_OR_PUSH`
    - `GameplayCameraComponentActivationMode.PUSH`
    - `GameplayCameraComponentActivationMode.PUSH_AND_INSERT`
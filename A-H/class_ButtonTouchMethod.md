# unreal.ButtonTouchMethod

```python
class unreal.ButtonTouchMethod
```


**Bases:** ``EnumBase``


Ways in which touch interactions trigger a “Clicked” event.

**C++ Source:**

- **Module**: SlateCore

- **File**: SlateEnums.h


DOWN _: ButtonTouchMethod_ _=Ellipsis_

Click will be triggered immediately on touch down, and touch will not be captured.

**Type:**

1

DOWN\_AND\_UP _: ButtonTouchMethod_ _=Ellipsis_

Most buttons behave this way.

**Type:**

0

PRECISE\_TAP _: ButtonTouchMethod_ _=Ellipsis_

Inside a list, buttons can only be clicked with precise tap.
Moving the pointer will scroll the list.

**Type:**

2

### Table of Contents

- `unreal.ButtonTouchMethod`
  - `ButtonTouchMethod`
    - `ButtonTouchMethod.DOWN`
    - `ButtonTouchMethod.DOWN_AND_UP`
    - `ButtonTouchMethod.PRECISE_TAP`
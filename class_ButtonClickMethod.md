# unreal.ButtonClickMethod

```python
class unreal.ButtonClickMethod
```


**Bases:** ``EnumBase``


Enumerates different methods that a button click can be triggered. Normally, DownAndUp is appropriate.

**C++ Source:**

- **Module**: SlateCore

- **File**: SlateEnums.h


DOWN\_AND\_UP _: ButtonClickMethod_ _=Ellipsis_

User must press the button, then release while over the button to trigger the click.
This is the most common type of button.

**Type:**

0

MOUSE\_DOWN _: ButtonClickMethod_ _=Ellipsis_

Click will be triggered immediately on mouse down, and mouse will not be captured.

**Type:**

1

MOUSE\_UP _: ButtonClickMethod_ _=Ellipsis_

Click will always be triggered when mouse button is released over the button,
even if the button wasn’t pressed down over it.

**Type:**

2

PRECISE\_CLICK _: ButtonClickMethod_ _=Ellipsis_

Inside a list, buttons can only be clicked with precise tap.
Moving the pointer will scroll the list, also allows drag-droppable buttons.

**Type:**

3

### Table of Contents

- `unreal.ButtonClickMethod`
  - `ButtonClickMethod`
    - `ButtonClickMethod.DOWN_AND_UP`
    - `ButtonClickMethod.MOUSE_DOWN`
    - `ButtonClickMethod.MOUSE_UP`
    - `ButtonClickMethod.PRECISE_CLICK`
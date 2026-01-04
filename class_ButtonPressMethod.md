# unreal.ButtonPressMethod

```python
class unreal.ButtonPressMethod
```


**Bases:** ``EnumBase``


Enumerates different methods that a button can be triggered with keyboard/controller. Normally, DownAndUp is appropriate.

**C++ Source:**

- **Module**: SlateCore

- **File**: SlateEnums.h


BUTTON\_PRESS _: ButtonPressMethod_ _=Ellipsis_

Click will be triggered immediately on button press.

**Type:**

1

BUTTON\_RELEASE _: ButtonPressMethod_ _=Ellipsis_

Click will always be triggered when a button release occurs on the focused button,
even if the button wasn’t pressed while focused.

**Type:**

2

DOWN\_AND\_UP _: ButtonPressMethod_ _=Ellipsis_

User must press the button, then release while the button has focus to trigger the click.
This is the most common type of button.

**Type:**

0

### Table of Contents

- `unreal.ButtonPressMethod`
  - `ButtonPressMethod`
    - `ButtonPressMethod.BUTTON_PRESS`
    - `ButtonPressMethod.BUTTON_RELEASE`
    - `ButtonPressMethod.DOWN_AND_UP`
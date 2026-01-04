# unreal.SelectionMode

```python
class unreal.SelectionMode
```


**Bases:** ``EnumBase``


ESelection Mode

**C++ Source:**

- **Module**: Slate

- **File**: ITypedTableView.h


MULTI _: SelectionMode_ _=Ellipsis_

Multiple items can be selected at the same time.

**Type:**

3

NONE _: SelectionMode_ _=Ellipsis_

Nothing can be selected and there is no hover cue for selection. You can still handle mouse button events though.

**Type:**

0

SINGLE _: SelectionMode_ _=Ellipsis_

A single item can be selected at once, or no item may be selected.

**Type:**

1

SINGLE\_TOGGLE _: SelectionMode_ _=Ellipsis_

A single item can be selected at once, or no item may be selected. You can click the item to toggle selection on and off.

**Type:**

2

### Table of Contents

- `unreal.SelectionMode`
  - `SelectionMode`
    - `SelectionMode.MULTI`
    - `SelectionMode.NONE`
    - `SelectionMode.SINGLE`
    - `SelectionMode.SINGLE_TOGGLE`
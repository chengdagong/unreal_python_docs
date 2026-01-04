# unreal.DragDropOperation

```python
class unreal.DragDropOperation(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


This class is the base drag drop operation for UMG, extend it to add additional data and add new functionality.

**C++ Source:**

- **Module**: UMG

- **File**: DragDropOperation.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `default_drag_visual` (Widget): [Read-Write] The Drag Visual is the widget to display when dragging the item. Normally people create a new widget to represent the
temporary drag.

- `offset` (Vector2D): [Read-Write] A percentage offset (-1..+1) from the Pivot location, the percentage is of the desired size of the dragged visual.

- `on_drag_cancelled` (OnDragDropMulticast): [Read-Write]

- `on_dragged` (OnDragDropMulticast): [Read-Write]

- `on_drop` (OnDragDropMulticast): [Read-Write]

- `payload` (Object): [Read-Write] The payload of the drag operation. This can be any UObject that you want to pass along as dragged data. If you
were building an inventory screen this would be the UObject representing the item being moved to another slot.

- `pivot` (DragPivot): [Read-Write] Controls where the drag widget visual will appear when dragged relative to the pointer performing
the drag operation.

- `tag` (str): [Read-Write] A simple string tag you can optionally use to provide extra metadata about the operation.



---

_property_ `default_drag_visual`: Widget

[Read-Only] The Drag Visual is the widget to display when dragging the item. Normally people create a new widget to represent the
temporary drag.

**Type:**

( Widget)


---

**drag_cancelled**( _pointer_event_) → `None`

Drag Cancelled

Parameters:

**pointer\_event** ( _PointerEvent_)


---

**dragged**( _pointer_event_) → `None`

Dragged

Parameters:

**pointer\_event** ( _PointerEvent_)


---

**drop**( _pointer_event_) → `None`

Drop

Parameters:

**pointer\_event** ( _PointerEvent_)


---

_property_ `offset`: Vector2D

[Read-Write] A percentage offset (-1..+1) from the Pivot location, the percentage is of the desired size of the dragged visual.

**Type:**

( Vector2D)


---

_property_ `on_drag_cancelled`: OnDragDropMulticast

[Read-Write]

**Type:**

( OnDragDropMulticast)


---

_property_ `on_dragged`: OnDragDropMulticast

[Read-Write]

**Type:**

( OnDragDropMulticast)


---

_property_ `on_drop`: OnDragDropMulticast

[Read-Write]

**Type:**

( OnDragDropMulticast)


---

_property_ `payload`: Object

[Read-Write] The payload of the drag operation. This can be any UObject that you want to pass along as dragged data. If you
were building an inventory screen this would be the UObject representing the item being moved to another slot.

**Type:**

( Object)


---

_property_ `pivot`: DragPivot

[Read-Write] Controls where the drag widget visual will appear when dragged relative to the pointer performing
the drag operation.

**Type:**

( DragPivot)


---

_property_ `tag`: str

[Read-Write] A simple string tag you can optionally use to provide extra metadata about the operation.

**Type:**

( str)

### Table of Contents

- `unreal.DragDropOperation`
  - `DragDropOperation`
    - `DragDropOperation.default_drag_visual`
    - `DragDropOperation.drag_cancelled()`
    - `DragDropOperation.dragged()`
    - `DragDropOperation.drop()`
    - `DragDropOperation.offset`
    - `DragDropOperation.on_drag_cancelled`
    - `DragDropOperation.on_dragged`
    - `DragDropOperation.on_drop`
    - `DragDropOperation.payload`
    - `DragDropOperation.pivot`
    - `DragDropOperation.tag`
# unreal.AnchorData

```python
class unreal.AnchorData(offsets:Margin=Ellipsis, anchors:Anchors=Ellipsis, alignment:Vector2D=Ellipsis)
```


**Bases:** ``StructBase``


Anchor Data

**C++ Source:**

- **Module**: UMG

- **File**: CanvasPanelSlot.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alignment` (Vector2D): [Read-Write] Alignment is the pivot point of the widget. Starting in the upper left at (0,0),
ending in the lower right at (1,1). Moving the alignment point allows you to move
the origin of the widget.

- `anchors` (Anchors): [Read-Write] Anchors.

- `offsets` (Margin): [Read-Write] Offset.



---

_property_ `alignment`: Vector2D

[Read-Write] Alignment is the pivot point of the widget. Starting in the upper left at (0,0),
ending in the lower right at (1,1). Moving the alignment point allows you to move
the origin of the widget.

**Type:**

( Vector2D)


---

_property_ `anchors`: Anchors

[Read-Write] Anchors.

**Type:**

( Anchors)


---

_property_ `offsets`: Margin

[Read-Write] Offset.

**Type:**

( Margin)

### Table of Contents

- `unreal.AnchorData`
  - `AnchorData`
    - `AnchorData.alignment`
    - `AnchorData.anchors`
    - `AnchorData.offsets`
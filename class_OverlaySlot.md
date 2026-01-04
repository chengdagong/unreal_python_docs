# unreal.OverlaySlot

```python
class unreal.OverlaySlot(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``PanelSlot``


Slot for the UOverlay panel. Allows content to be hover above other content.

**C++ Source:**

- **Module**: UMG

- **File**: OverlaySlot.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `horizontal_alignment` (HorizontalAlignment): [Read-Write] The alignment of the object horizontally.

- `padding` (Margin): [Read-Write] The padding area between the slot and the content it contains.

- `vertical_alignment` (VerticalAlignment): [Read-Write] The alignment of the object vertically.



---

_property_ `horizontal_alignment`: HorizontalAlignment

[Read-Write] The alignment of the object horizontally.

**Type:**

( HorizontalAlignment)


---

_property_ `padding`: Margin

[Read-Write] The padding area between the slot and the content it contains.

**Type:**

( Margin)


---

**set_horizontal_alignment**( _horizontal_alignment_) → `None`

Set the alignment of the object horizontally.

Parameters:

**horizontal\_alignment** ( _HorizontalAlignment_)


---

**set_padding**( _padding_) → `None`

Set padding area between the slot and the content it contains.

Parameters:

**padding** ( _Margin_)


---

**set_vertical_alignment**( _vertical_alignment_) → `None`

Set the alignment of the object vertically.

Parameters:

**vertical\_alignment** ( _VerticalAlignment_)


---

_property_ `vertical_alignment`: VerticalAlignment

[Read-Write] The alignment of the object vertically.

**Type:**

( VerticalAlignment)

### Table of Contents

- `unreal.OverlaySlot`
  - `OverlaySlot`
    - `OverlaySlot.horizontal_alignment`
    - `OverlaySlot.padding`
    - `OverlaySlot.set_horizontal_alignment()`
    - `OverlaySlot.set_padding()`
    - `OverlaySlot.set_vertical_alignment()`
    - `OverlaySlot.vertical_alignment`
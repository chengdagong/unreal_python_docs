# unreal.Throbber

```python
class unreal.Throbber(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Widget``


A Throbber widget that shows several zooming circles in a row.

**C++ Source:**

- **Module**: UMG

- **File**: Throbber.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `accessible_behavior` (SlateAccessibleBehavior): [Read-Write] Whether or not the widget is accessible, and how to describe it. If set to custom, additional customization options will appear.

- `accessible_summary_behavior` (SlateAccessibleBehavior): [Read-Write] How to describe this widget when it’s being presented through a summary of a parent widget. If set to custom, additional customization options will appear.

- `accessible_summary_text` (Text): [Read-Write] When AccessibleSummaryBehavior is set to Custom, this is the text that will be used to describe the widget.

- `accessible_text` (Text): [Read-Write] When AccessibleBehavior is set to Custom, this is the text that will be used to describe the widget.

- `animate_horizontally` (bool): [Read-Write] Should the pieces animate horizontally?

- `animate_opacity` (bool): [Read-Write] Should the pieces animate their opacity?

- `animate_vertically` (bool): [Read-Write] Should the pieces animate vertically?

- `can_children_be_accessible` (bool): [Read-Write] Whether or not children of this widget can appear as distinct accessible widgets.

- `clipping` (WidgetClipping): [Read-Write] Controls how the clipping behavior of this widget. Normally content that overflows the
bounds of the widget continues rendering. Enabling clipping prevents that overflowing content
from being seen.

NOTE: Elements in different clipping spaces can not be batched together, and so there is a
performance cost to clipping. Do not enable clipping unless a panel actually needs to prevent
content from showing up outside its bounds.

- `cursor` (MouseCursor): [Read-Write] The cursor to show when the mouse is over the widget

- `flow_direction_preference` (FlowDirectionPreference): [Read-Write] Allows you to set a new flow direction

- `image` (SlateBrush): [Read-Write] The animated pieces.

- `is_enabled` (bool): [Read-Write] Sets whether this widget can be modified interactively by the user

- `is_volatile` (bool): [Read-Write] If true prevents the widget or its child’s geometry or layout information from being cached. If this widget
changes every frame, but you want it to still be in an invalidation panel you should make it as volatile
instead of invalidating it every frame, which would prevent the invalidation panel from actually
ever caching anything.

- `navigation` (WidgetNavigation): [Read-Write] The navigation object for this widget is optionally created if the user has configured custom
navigation rules for this widget in the widget designer. Those rules determine how navigation transitions
can occur between widgets.

- `number_of_pieces` (int32): [Read-Write] How many pieces there are

- `override_accessible_defaults` (bool): [Read-Write] Override all of the default accessibility behavior and text for this widget.

- `override_cursor` (bool): [Read-Write]

- `pixel_snapping` (WidgetPixelSnapping): [Read-Write] If the widget will draw snapped to the nearest pixel. Improves clarity but might cause visibile stepping in animation

- `render_opacity` (float): [Read-Write] The opacity of the widget

- `render_transform` (WidgetTransform): [Read-Write] The render transform of the widget allows for arbitrary 2D transforms to be applied to the widget.

- `render_transform_pivot` (Vector2D): [Read-Write] The render transform pivot controls the location about which transforms are applied.
This value is a normalized coordinate about which things like rotations will occur.

- `slot` (PanelSlot): [Read-Write] The parent slot of the UWidget. Allows us to easily inline edit the layout controlling this widget.

- `tool_tip_text` (Text): [Read-Write] Tooltip text to show when the user hovers over the widget with the mouse

- `tool_tip_widget` (Widget): [Read-Only] Tooltip widget to show when the user hovers over the widget with the mouse

- `visibility` (SlateVisibility): [Read-Write] The visibility of the widget



---

_property_ `animate_horizontally`: bool

[Read-Write] Should the pieces animate horizontally?

**Type:**

( bool)


---

_property_ `animate_opacity`: bool

[Read-Write] Should the pieces animate their opacity?

**Type:**

( bool)


---

_property_ `animate_vertically`: bool

[Read-Write] Should the pieces animate vertically?

**Type:**

( bool)


---

_property_ `image`: SlateBrush

[Read-Write] The animated pieces.

**Type:**

( SlateBrush)


---

_property_ `number_of_pieces`: int

[Read-Write] How many pieces there are

**Type:**

(int32)


---

**set_animate_horizontally**( _animate_horizontally_) → `None`

Sets whether the pieces animate horizontally.

Parameters:

**animate\_horizontally** ( _bool_)


---

**set_animate_opacity**( _animate_opacity_) → `None`

Sets whether the pieces animate their opacity.

Parameters:

**animate\_opacity** ( _bool_)


---

**set_animate_vertically**( _animate_vertically_) → `None`

Sets whether the pieces animate vertically.

Parameters:

**animate\_vertically** ( _bool_)


---

**set_number_of_pieces**( _number_of_pieces_) → `None`

Sets how many pieces there are

Parameters:

**number\_of\_pieces** ( _int32_)

### Table of Contents

- `unreal.Throbber`
  - `Throbber`
    - `Throbber.animate_horizontally`
    - `Throbber.animate_opacity`
    - `Throbber.animate_vertically`
    - `Throbber.image`
    - `Throbber.number_of_pieces`
    - `Throbber.set_animate_horizontally()`
    - `Throbber.set_animate_opacity()`
    - `Throbber.set_animate_vertically()`
    - `Throbber.set_number_of_pieces()`
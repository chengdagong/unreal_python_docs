# unreal.SizeBox

```python
class unreal.SizeBox(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``ContentWidget``


A widget that allows you to specify the size it reports to have and desire. Not all widgets report a desired size
that you actually desire. Wrapping them in a SizeBox lets you have the Size Box force them to be a particular size.

- Single Child

- Fixed Size


**C++ Source:**

- **Module**: UMG

- **File**: SizeBox.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `accessible_behavior` (SlateAccessibleBehavior): [Read-Write] Whether or not the widget is accessible, and how to describe it. If set to custom, additional customization options will appear.

- `accessible_summary_behavior` (SlateAccessibleBehavior): [Read-Write] How to describe this widget when it’s being presented through a summary of a parent widget. If set to custom, additional customization options will appear.

- `accessible_summary_text` (Text): [Read-Write] When AccessibleSummaryBehavior is set to Custom, this is the text that will be used to describe the widget.

- `accessible_text` (Text): [Read-Write] When AccessibleBehavior is set to Custom, this is the text that will be used to describe the widget.

- `can_children_be_accessible` (bool): [Read-Write] Whether or not children of this widget can appear as distinct accessible widgets.

- `clipping` (WidgetClipping): [Read-Write] Controls how the clipping behavior of this widget. Normally content that overflows the
bounds of the widget continues rendering. Enabling clipping prevents that overflowing content
from being seen.

NOTE: Elements in different clipping spaces can not be batched together, and so there is a
performance cost to clipping. Do not enable clipping unless a panel actually needs to prevent
content from showing up outside its bounds.

- `cursor` (MouseCursor): [Read-Write] The cursor to show when the mouse is over the widget

- `flow_direction_preference` (FlowDirectionPreference): [Read-Write] Allows you to set a new flow direction

- `height_override` (float): [Read-Write] When specified, ignore the content’s desired size and report the HeightOverride as the Box’s desired height.

- `is_enabled` (bool): [Read-Write] Sets whether this widget can be modified interactively by the user

- `is_volatile` (bool): [Read-Write] If true prevents the widget or its child’s geometry or layout information from being cached. If this widget
changes every frame, but you want it to still be in an invalidation panel you should make it as volatile
instead of invalidating it every frame, which would prevent the invalidation panel from actually
ever caching anything.

- `max_aspect_ratio` (float): [Read-Write]

- `max_desired_height` (float): [Read-Write] When specified, will report the MaxDesiredHeight if smaller than the content’s desired height.

- `max_desired_width` (float): [Read-Write] When specified, will report the MaxDesiredWidth if smaller than the content’s desired width.

- `min_aspect_ratio` (float): [Read-Write]

- `min_desired_height` (float): [Read-Write] When specified, will report the MinDesiredHeight if larger than the content’s desired height.

- `min_desired_width` (float): [Read-Write] When specified, will report the MinDesiredWidth if larger than the content’s desired width.

- `navigation` (WidgetNavigation): [Read-Write] The navigation object for this widget is optionally created if the user has configured custom
navigation rules for this widget in the widget designer. Those rules determine how navigation transitions
can occur between widgets.

- `override_accessible_defaults` (bool): [Read-Write] Override all of the default accessibility behavior and text for this widget.

- `override_cursor` (bool): [Read-Write]

- `override_height_override` (bool): [Read-Write]

- `override_max_aspect_ratio` (bool): [Read-Write]

- `override_max_desired_height` (bool): [Read-Write]

- `override_max_desired_width` (bool): [Read-Write]

- `override_min_aspect_ratio` (bool): [Read-Write]

- `override_min_desired_height` (bool): [Read-Write]

- `override_min_desired_width` (bool): [Read-Write]

- `override_width_override` (bool): [Read-Write]

- `pixel_snapping` (WidgetPixelSnapping): [Read-Write] If the widget will draw snapped to the nearest pixel. Improves clarity but might cause visibile stepping in animation

- `render_opacity` (float): [Read-Write] The opacity of the widget

- `render_transform` (WidgetTransform): [Read-Write] The render transform of the widget allows for arbitrary 2D transforms to be applied to the widget.

- `render_transform_pivot` (Vector2D): [Read-Write] The render transform pivot controls the location about which transforms are applied.
This value is a normalized coordinate about which things like rotations will occur.

- `slot` (PanelSlot): [Read-Write] The parent slot of the UWidget. Allows us to easily inline edit the layout controlling this widget.

- `tool_tip_text` (Text): [Read-Write] Tooltip text to show when the user hovers over the widget with the mouse

- `tool_tip_widget` (Widget): [Read-Only] Tooltip widget to show when the user hovers over the widget with the mouse

- `visibility` (SlateVisibility): [Read-Write] The visibility of the widget

- `width_override` (float): [Read-Write] When specified, ignore the content’s desired size and report the WidthOverride as the Box’s desired width.



---

**clear_height_override**() → `None`

Clear Height Override


---

**clear_max_aspect_ratio**() → `None`

Clear Max Aspect Ratio


---

**clear_max_desired_height**() → `None`

Clear Max Desired Height


---

**clear_max_desired_width**() → `None`

Clear Max Desired Width


---

**clear_min_aspect_ratio**() → `None`

Clear Min Aspect Ratio


---

**clear_min_desired_height**() → `None`

Clear Min Desired Height


---

**clear_min_desired_width**() → `None`

Clear Min Desired Width


---

**clear_width_override**() → `None`

Clear Width Override


---

_property_ `height_override`: float

[Read-Write] When specified, ignore the content’s desired size and report the HeightOverride as the Box’s desired height.

**Type:**

( float)


---

_property_ `max_aspect_ratio`: float

[Read-Write]

**Type:**

( float)


---

_property_ `max_desired_height`: float

[Read-Write] When specified, will report the MaxDesiredHeight if smaller than the content’s desired height.

**Type:**

( float)


---

_property_ `max_desired_width`: float

[Read-Write] When specified, will report the MaxDesiredWidth if smaller than the content’s desired width.

**Type:**

( float)


---

_property_ `min_aspect_ratio`: float

[Read-Write]

**Type:**

( float)


---

_property_ `min_desired_height`: float

[Read-Write] When specified, will report the MinDesiredHeight if larger than the content’s desired height.

**Type:**

( float)


---

_property_ `min_desired_width`: float

[Read-Write] When specified, will report the MinDesiredWidth if larger than the content’s desired width.

**Type:**

( float)


---

**set_height_override**( _height_override_) → `None`

When specified, ignore the content’s desired size and report the HeightOverride as the Box’s desired height.

Parameters:

**height\_override** ( _float_)


---

**set_max_aspect_ratio**( _max_aspect_ratio_) → `None`

Set Max Aspect Ratio

Parameters:

**max\_aspect\_ratio** ( _float_)


---

**set_max_desired_height**( _max_desired_height_) → `None`

When specified, will report the MaxDesiredHeight if smaller than the content’s desired height.

Parameters:

**max\_desired\_height** ( _float_)


---

**set_max_desired_width**( _max_desired_width_) → `None`

When specified, will report the MaxDesiredWidth if smaller than the content’s desired width.

Parameters:

**max\_desired\_width** ( _float_)


---

**set_min_aspect_ratio**( _min_aspect_ratio_) → `None`

Set Min Aspect Ratio

Parameters:

**min\_aspect\_ratio** ( _float_)


---

**set_min_desired_height**( _min_desired_height_) → `None`

When specified, will report the MinDesiredHeight if larger than the content’s desired height.

Parameters:

**min\_desired\_height** ( _float_)


---

**set_min_desired_width**( _min_desired_width_) → `None`

When specified, will report the MinDesiredWidth if larger than the content’s desired width.

Parameters:

**min\_desired\_width** ( _float_)


---

**set_width_override**( _width_override_) → `None`

When specified, ignore the content’s desired size and report the WidthOverride as the Box’s desired width.

Parameters:

**width\_override** ( _float_)


---

_property_ `width_override`: float

[Read-Write] When specified, ignore the content’s desired size and report the WidthOverride as the Box’s desired width.

**Type:**

( float)

### Table of Contents

- `unreal.SizeBox`
  - `SizeBox`
    - `SizeBox.clear_height_override()`
    - `SizeBox.clear_max_aspect_ratio()`
    - `SizeBox.clear_max_desired_height()`
    - `SizeBox.clear_max_desired_width()`
    - `SizeBox.clear_min_aspect_ratio()`
    - `SizeBox.clear_min_desired_height()`
    - `SizeBox.clear_min_desired_width()`
    - `SizeBox.clear_width_override()`
    - `SizeBox.height_override`
    - `SizeBox.max_aspect_ratio`
    - `SizeBox.max_desired_height`
    - `SizeBox.max_desired_width`
    - `SizeBox.min_aspect_ratio`
    - `SizeBox.min_desired_height`
    - `SizeBox.min_desired_width`
    - `SizeBox.set_height_override()`
    - `SizeBox.set_max_aspect_ratio()`
    - `SizeBox.set_max_desired_height()`
    - `SizeBox.set_max_desired_width()`
    - `SizeBox.set_min_aspect_ratio()`
    - `SizeBox.set_min_desired_height()`
    - `SizeBox.set_min_desired_width()`
    - `SizeBox.set_width_override()`
    - `SizeBox.width_override`
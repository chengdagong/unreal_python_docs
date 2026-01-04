# unreal.ProgressBar

```python
class unreal.ProgressBar(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Widget``


The progress bar widget is a simple bar that fills up that can be restyled to fit any number of uses.

- No Children


**C++ Source:**

- **Module**: UMG

- **File**: ProgressBar.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `accessible_behavior` (SlateAccessibleBehavior): [Read-Write] Whether or not the widget is accessible, and how to describe it. If set to custom, additional customization options will appear.

- `accessible_summary_behavior` (SlateAccessibleBehavior): [Read-Write] How to describe this widget when it’s being presented through a summary of a parent widget. If set to custom, additional customization options will appear.

- `accessible_summary_text` (Text): [Read-Write] When AccessibleSummaryBehavior is set to Custom, this is the text that will be used to describe the widget.

- `accessible_text` (Text): [Read-Write] When AccessibleBehavior is set to Custom, this is the text that will be used to describe the widget.

- `bar_fill_style` (ProgressBarFillStyle): [Read-Write] Defines the visual style of the progress bar fill - scale or mask

- `bar_fill_type` (ProgressBarFillType): [Read-Write] Defines the direction in which the progress bar fills

- `border_padding` (Vector2D): [Read-Write]

- `can_children_be_accessible` (bool): [Read-Write] Whether or not children of this widget can appear as distinct accessible widgets.

- `clipping` (WidgetClipping): [Read-Write] Controls how the clipping behavior of this widget. Normally content that overflows the
bounds of the widget continues rendering. Enabling clipping prevents that overflowing content
from being seen.

NOTE: Elements in different clipping spaces can not be batched together, and so there is a
performance cost to clipping. Do not enable clipping unless a panel actually needs to prevent
content from showing up outside its bounds.

- `cursor` (MouseCursor): [Read-Write] The cursor to show when the mouse is over the widget

- `fill_color_and_opacity` (LinearColor): [Read-Write] Fill Color and Opacity

- `flow_direction_preference` (FlowDirectionPreference): [Read-Write] Allows you to set a new flow direction

- `is_enabled` (bool): [Read-Write] Sets whether this widget can be modified interactively by the user

- `is_marquee` (bool): [Read-Write]

- `is_volatile` (bool): [Read-Write] If true prevents the widget or its child’s geometry or layout information from being cached. If this widget
changes every frame, but you want it to still be in an invalidation panel you should make it as volatile
instead of invalidating it every frame, which would prevent the invalidation panel from actually
ever caching anything.

- `navigation` (WidgetNavigation): [Read-Write] The navigation object for this widget is optionally created if the user has configured custom
navigation rules for this widget in the widget designer. Those rules determine how navigation transitions
can occur between widgets.

- `override_accessible_defaults` (bool): [Read-Write] Override all of the default accessibility behavior and text for this widget.

- `override_cursor` (bool): [Read-Write]

- `percent` (float): [Read-Write] Used to determine the fill position of the progress bar ranging 0..1

- `pixel_snapping` (WidgetPixelSnapping): [Read-Write] If the widget will draw snapped to the nearest pixel. Improves clarity but might cause visibile stepping in animation

- `render_opacity` (float): [Read-Write] The opacity of the widget

- `render_transform` (WidgetTransform): [Read-Write] The render transform of the widget allows for arbitrary 2D transforms to be applied to the widget.

- `render_transform_pivot` (Vector2D): [Read-Write] The render transform pivot controls the location about which transforms are applied.
This value is a normalized coordinate about which things like rotations will occur.

- `slot` (PanelSlot): [Read-Write] The parent slot of the UWidget. Allows us to easily inline edit the layout controlling this widget.

- `tool_tip_text` (Text): [Read-Write] Tooltip text to show when the user hovers over the widget with the mouse

- `tool_tip_widget` (Widget): [Read-Only] Tooltip widget to show when the user hovers over the widget with the mouse

- `visibility` (SlateVisibility): [Read-Write] The visibility of the widget

- `widget_style` (ProgressBarStyle): [Read-Write] The progress bar style



---

_property_ `bar_fill_style`: ProgressBarFillStyle

[Read-Write] Defines the visual style of the progress bar fill - scale or mask

**Type:**

( ProgressBarFillStyle)


---

_property_ `bar_fill_type`: ProgressBarFillType

[Read-Write] Defines the direction in which the progress bar fills

**Type:**

( ProgressBarFillType)


---

_property_ `border_padding`: Vector2D

[Read-Write]

**Type:**

( Vector2D)


---

_property_ `fill_color_and_opacity`: LinearColor

[Read-Write] Fill Color and Opacity

**Type:**

( LinearColor)


---

_property_ `is_marquee`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `percent`: float

[Read-Write] Used to determine the fill position of the progress bar ranging 0..1

**Type:**

( float)


---

**set_fill_color_and_opacity**( _color_) → `None`

Sets the fill color of the progress bar.

Parameters:

**color** ( _LinearColor_)


---

**set_is_marquee**( _inb_is_marquee_) → `None`

Sets the progress bar to show as a marquee.

Parameters:

**inb\_is\_marquee** ( _bool_)


---

**set_percent**( _percent_) → `None`

Sets the current value of the ProgressBar.

Parameters:

**percent** ( _float_)


---

_property_ `widget_style`: ProgressBarStyle

[Read-Write] The progress bar style

**Type:**

( ProgressBarStyle)

### Table of Contents

- `unreal.ProgressBar`
  - `ProgressBar`
    - `ProgressBar.bar_fill_style`
    - `ProgressBar.bar_fill_type`
    - `ProgressBar.border_padding`
    - `ProgressBar.fill_color_and_opacity`
    - `ProgressBar.is_marquee`
    - `ProgressBar.percent`
    - `ProgressBar.set_fill_color_and_opacity()`
    - `ProgressBar.set_is_marquee()`
    - `ProgressBar.set_percent()`
    - `ProgressBar.widget_style`
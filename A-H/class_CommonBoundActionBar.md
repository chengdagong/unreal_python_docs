# unreal.CommonBoundActionBar

```python
class unreal.CommonBoundActionBar(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``DynamicEntryBoxBase``


A box populated with current actions available per CommonUI’s Input Handler.

**C++ Source:**

- **Plugin**: CommonUI

- **Module**: CommonUI

- **File**: CommonBoundActionBar.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `accessible_behavior` (SlateAccessibleBehavior): [Read-Write] Whether or not the widget is accessible, and how to describe it. If set to custom, additional customization options will appear.

- `accessible_summary_behavior` (SlateAccessibleBehavior): [Read-Write] How to describe this widget when it’s being presented through a summary of a parent widget. If set to custom, additional customization options will appear.

- `accessible_summary_text` (Text): [Read-Write] When AccessibleSummaryBehavior is set to Custom, this is the text that will be used to describe the widget.

- `accessible_text` (Text): [Read-Write] When AccessibleBehavior is set to Custom, this is the text that will be used to describe the widget.

- `action_button_class` (type(Class)): [Read-Write]

- `can_children_be_accessible` (bool): [Read-Write] Whether or not children of this widget can appear as distinct accessible widgets.

- `clipping` (WidgetClipping): [Read-Write] Controls how the clipping behavior of this widget. Normally content that overflows the
bounds of the widget continues rendering. Enabling clipping prevents that overflowing content
from being seen.

NOTE: Elements in different clipping spaces can not be batched together, and so there is a
performance cost to clipping. Do not enable clipping unless a panel actually needs to prevent
content from showing up outside its bounds.

- `cursor` (MouseCursor): [Read-Write] The cursor to show when the mouse is over the widget

- `display_owning_player_actions_only` (bool): [Read-Write]

- `entry_box_type` (DynamicBoxType): [Read-Write] The type of box panel into which created entries are added. Some differences in functionality exist between each type.

- `entry_horizontal_alignment` (HorizontalAlignment): [Read-Write] Horizontal alignment of generated entries. Horizontal/Vertical/Wrap boxes only.

- `entry_size_rule` (SlateChildSize): [Read-Write] Sizing rule to apply to generated entries. Horizontal/Vertical boxes only.

- `entry_spacing` (Vector2D): [Read-Write] The padding to apply between entries in the box.
Note horizontal boxes only use the X and vertical boxes only use Y. Value is also ignored for the first entry in the box.
Wrap and Overlay types use both X and Y for spacing.

- `entry_vertical_alignment` (VerticalAlignment): [Read-Write] Vertical alignment of generated entries. Horizontal/Vertical/Wrap boxes only.

- `flow_direction_preference` (FlowDirectionPreference): [Read-Write] Allows you to set a new flow direction

- `ignore_duplicate_actions` (bool): [Read-Write]

- `is_enabled` (bool): [Read-Write] Sets whether this widget can be modified interactively by the user

- `is_volatile` (bool): [Read-Write] If true prevents the widget or its child’s geometry or layout information from being cached. If this widget
changes every frame, but you want it to still be in an invalidation panel you should make it as volatile
instead of invalidating it every frame, which would prevent the invalidation panel from actually
ever caching anything.

- `max_element_size` (int32): [Read-Write] The maximum size of each entry in the dominant axis of the box. Vertical/Horizontal boxes only.

- `navigation` (WidgetNavigation): [Read-Write] The navigation object for this widget is optionally created if the user has configured custom
navigation rules for this widget in the widget designer. Those rules determine how navigation transitions
can occur between widgets.

- `on_action_bar_updated` (ActionBarUpdated): [Read-Write]

- `override_accessible_defaults` (bool): [Read-Write] Override all of the default accessibility behavior and text for this widget.

- `override_cursor` (bool): [Read-Write]

- `pixel_snapping` (WidgetPixelSnapping): [Read-Write] If the widget will draw snapped to the nearest pixel. Improves clarity but might cause visibile stepping in animation

- `radial_box_settings` (RadialBoxSettings): [Read-Write] Settings only relevant to RadialBox

- `render_opacity` (float): [Read-Write] The opacity of the widget

- `render_transform` (WidgetTransform): [Read-Write] The render transform of the widget allows for arbitrary 2D transforms to be applied to the widget.

- `render_transform_pivot` (Vector2D): [Read-Write] The render transform pivot controls the location about which transforms are applied.
This value is a normalized coordinate about which things like rotations will occur.

- `slot` (PanelSlot): [Read-Write] The parent slot of the UWidget. Allows us to easily inline edit the layout controlling this widget.

- `spacing_pattern` (Array[Vector2D]): [Read-Write] The looping sequence of entry paddings to apply as entries are created. Overlay boxes only. Ignores EntrySpacing if not empty.

- `tool_tip_text` (Text): [Read-Write] Tooltip text to show when the user hovers over the widget with the mouse

- `tool_tip_widget` (Widget): [Read-Only] Tooltip widget to show when the user hovers over the widget with the mouse

- `visibility` (SlateVisibility): [Read-Write] The visibility of the widget



---

_property_ `on_action_bar_updated`: ActionBarUpdated

[Read-Write]

**Type:**

( ActionBarUpdated)


---

**set_display_owning_player_actions_only**( _should_only_display_owning_player_actions_) → `None`

Set Display Owning Player Actions Only

Parameters:

**should\_only\_display\_owning\_player\_actions** ( _bool_)

### Table of Contents

- `unreal.CommonBoundActionBar`
  - `CommonBoundActionBar`
    - `CommonBoundActionBar.on_action_bar_updated`
    - `CommonBoundActionBar.set_display_owning_player_actions_only()`
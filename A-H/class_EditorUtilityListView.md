# unreal.EditorUtilityListView

```python
class unreal.EditorUtilityListView(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``ListView``


Editor Utility List View

**C++ Source:**

- **Module**: Blutility

- **File**: EditorUtilityWidgetComponents.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `accessible_behavior` (SlateAccessibleBehavior): [Read-Write] Whether or not the widget is accessible, and how to describe it. If set to custom, additional customization options will appear.

- `accessible_summary_behavior` (SlateAccessibleBehavior): [Read-Write] How to describe this widget when it’s being presented through a summary of a parent widget. If set to custom, additional customization options will appear.

- `accessible_summary_text` (Text): [Read-Write] When AccessibleSummaryBehavior is set to Custom, this is the text that will be used to describe the widget.

- `accessible_text` (Text): [Read-Write] When AccessibleBehavior is set to Custom, this is the text that will be used to describe the widget.

- `allow_drag_drop` (bool): [Read-Write] Allow drag and drop operations to be performed on the list.

- `allow_dragging` (bool): [Read-Write] True to allow dragging of row widgets in the list

- `allow_keep_preselected_items` (bool): [Read-Write] If true, when selecting an item via mouse button, we allow pre-selected items to remain selected (applicable to “Multi” Selection Mode only).

- `allow_overscroll` (bool): [Read-Write] Disable to stop scrollbars from activating inertial overscrolling

- `bp_on_entries_generated` (OnListEntriesGeneratedDynamic): [Read-Write] Called when all row widgets are generated for all list items

- `bp_on_entry_generated` (OnListEntryGeneratedDynamic): [Read-Write] Called when a row widget is generated for a list item

- `bp_on_entry_initialized` (OnListEntryInitializedDynamic): [Read-Write] Called when a row widget is generated for a list item

- `bp_on_entry_released` (OnListEntryReleasedDynamic): [Read-Write] Called when a row widget is released by the list (i.e. when it no longer represents a list item)

- `bp_on_is_item_selectable_or_navigable` (OnIsItemSelectableOrNavigableDynamic): [Read-Write]

- `bp_on_item_accept_drop` (OnItemZoneMulticastDynamic): [Read-Write]

- `bp_on_item_clicked` (SimpleListItemEventDynamic): [Read-Write]

- `bp_on_item_double_clicked` (SimpleListItemEventDynamic): [Read-Write]

- `bp_on_item_drag_cancelled` (OnItemDragCancelledDynamic): [Read-Write]

- `bp_on_item_drag_detected` (OnItemGeometryMulticastDynamic): [Read-Write]

- `bp_on_item_drag_enter` (OnItemDragDropMulticastDynamic): [Read-Write]

- `bp_on_item_drag_leave` (OnItemDragDropMulticastDynamic): [Read-Write]

- `bp_on_item_is_hovered_changed` (OnItemIsHoveredChangedDynamic): [Read-Write]

- `bp_on_item_scrolled_into_view` (OnListItemScrolledIntoViewDynamic): [Read-Write]

- `bp_on_item_selection_changed` (OnListItemSelectionChangedDynamic): [Read-Write]

- `bp_on_list_view_dragging_state_changed` (OnListViewDraggingStateChangedDynamic): [Read-Write]

- `bp_on_list_view_finished_scrolling` (OnListViewFinishedScrollingDynamic): [Read-Write]

- `bp_on_list_view_scrolled` (OnListViewScrolledDynamic): [Read-Write]

- `can_children_be_accessible` (bool): [Read-Write] Whether or not children of this widget can appear as distinct accessible widgets.

- `clear_scroll_velocity_on_selection` (bool): [Read-Write]

- `clear_selection_on_click` (bool): [Read-Write]

- `clipping` (WidgetClipping): [Read-Write] Controls how the clipping behavior of this widget. Normally content that overflows the
bounds of the widget continues rendering. Enabling clipping prevents that overflowing content
from being seen.

NOTE: Elements in different clipping spaces can not be batched together, and so there is a
performance cost to clipping. Do not enable clipping unless a panel actually needs to prevent
content from showing up outside its bounds.

- `consume_mouse_wheel` (ConsumeMouseWheel): [Read-Write]

- `cursor` (MouseCursor): [Read-Write] The cursor to show when the mouse is over the widget

- `drag_drop_operation_class` (type(Class)): [Read-Write] The drag drop operation class for this listview - if this is not specified, drag drop operations will not be created.

- `drag_drop_visual_entry_class` (type(Class)): [Read-Write] The class which will be used to generate the drag drop visual. If none is specified, the EntryWidgetClass will be used.

- `drag_drop_visual_offset` (Vector2D): [Read-Write] A percentage offset (-1..+1) from the Pivot location, the percentage is of the desired size of the dragged visual.

- `drag_drop_visual_pivot` (DragPivot): [Read-Write] Controls where the drag widget visual will appear when dragged relative to the pointer performing
the drag operation.

- `drag_visual_widget` (Widget): [Read-Write] This is the actual drag visual widget that will be used by the drag drop operation.This can be set in blueprint via override of CreateDragDropOperation(should call parent)

- `enable_fixed_line_offset` (bool): [Read-Write]

- `enable_right_click_scrolling` (bool): [Read-Write] True to allow right click drag scrolling.

- `enable_scroll_animation` (bool): [Read-Write] True to enable lerped animation when scrolling through the list

- `enable_shadow_brush` (bool): [Read-Write]

- `enable_touch_animated_scrolling` (bool): [Read-Write] True to enable lerped animation when scrolling through the list with touch

- `enable_touch_scrolling` (bool): [Read-Write] True to allow scrolling using touch input.

- `entry_spacing` (float): [Read-Write] This deprecated property was originally BlueprintReadOnly. To satisfy the compiler requirment to have a BlueprintGetter for this property,
it relies on the newly added UFunction GetHorizontalEntrySpacing() to act as its BlueprintGetter.
deprecated: EntrySpacing has been deprecated. Please use HorizontalEntrySpacing and VerticalEntrySpacing.

- `entry_widget_class` (type(Class)): [Read-Write] The type of widget to create for each entry displayed in the list.

- `fixed_line_scroll_offset` (float): [Read-Write] Optional fixed offset (in lines) to always apply to the top/left (depending on orientation) of the list.
If provided, all non-inertial means of scrolling will settle with exactly this offset of the topmost entry.
Ex: A value of 0.25 would cause the topmost full entry to be offset down by a quarter length of the preceeding entry.

- `flow_direction_preference` (FlowDirectionPreference): [Read-Write] Allows you to set a new flow direction

- `horizontal_entry_spacing` (float): [Read-Write]

- `is_dragging` (bool): [Read-Write] This indicates whether the ListViewBase is currently in a dragging state

- `is_enabled` (bool): [Read-Write] Sets whether this widget can be modified interactively by the user

- `is_focusable` (bool): [Read-Write]

- `is_gamepad_scrolling_enabled` (bool): [Read-Write] Enable/Disable scrolling using Gamepad.

- `is_pointer_scrolling_enabled` (bool): [Read-Write] Enable/Disable scrolling using Touch or Mouse.

- `is_volatile` (bool): [Read-Write] If true prevents the widget or its child’s geometry or layout information from being cached. If this widget
changes every frame, but you want it to still be in an invalidation panel you should make it as volatile
instead of invalidating it every frame, which would prevent the invalidation panel from actually
ever caching anything.

- `navigation` (WidgetNavigation): [Read-Write] The navigation object for this widget is optionally created if the user has configured custom
navigation rules for this widget in the widget designer. Those rules determine how navigation transitions
can occur between widgets.

- `num_designer_preview_entries` (int32): [Read-Write] The number of dummy item entry widgets to preview in the widget designer

- `orientation` (Orientation): [Read-Write] The scroll & layout orientation of the list. ListView and TileView only.
Vertical will scroll vertically and arrange tiles into rows.
Horizontal will scroll horizontally and arrange tiles into columns.

- `override_accessible_defaults` (bool): [Read-Write] Override all of the default accessibility behavior and text for this widget.

- `override_cursor` (bool): [Read-Write]

- `pixel_snapping` (WidgetPixelSnapping): [Read-Write] If the widget will draw snapped to the nearest pixel. Improves clarity but might cause visibile stepping in animation

- `render_opacity` (float): [Read-Write] The opacity of the widget

- `render_transform` (WidgetTransform): [Read-Write] The render transform of the widget allows for arbitrary 2D transforms to be applied to the widget.

- `render_transform_pivot` (Vector2D): [Read-Write] The render transform pivot controls the location about which transforms are applied.
This value is a normalized coordinate about which things like rotations will occur.

- `return_focus_to_selection` (bool): [Read-Write]

- `scroll_bar_padding` (Margin): [Read-Write]

- `scroll_bar_style` (ScrollBarStyle): [Read-Write]

- `scroll_into_view_alignment` (ScrollIntoViewAlignment): [Read-Write] Sets where to scroll a widget to when using explicit navigation

- `scrolling_animation_interpolation_speed` (float): [Read-Write] The speed to apply when lerping in the scroll animation.

- `select_item_on_navigation` (bool): [Read-Write] If true, items will be “selected” (in addition to focused) when navigating to them. If false, they will only be focused.

- `selection_mode` (SelectionMode): [Read-Write]

- `shadow_brush_style` (ScrollBoxStyle): [Read-Write]

- `slot` (PanelSlot): [Read-Write] The parent slot of the UWidget. Allows us to easily inline edit the layout controlling this widget.

- `tool_tip_text` (Text): [Read-Write] Tooltip text to show when the user hovers over the widget with the mouse

- `tool_tip_widget` (Widget): [Read-Only] Tooltip widget to show when the user hovers over the widget with the mouse

- `vertical_entry_spacing` (float): [Read-Write]

- `visibility` (SlateVisibility): [Read-Write] The visibility of the widget

- `wheel_scroll_multiplier` (float): [Read-Write] The multiplier to apply when wheel scrolling

- `widget_style` (TableViewStyle): [Read-Write]


### Table of Contents

- `unreal.EditorUtilityListView`
  - `EditorUtilityListView`
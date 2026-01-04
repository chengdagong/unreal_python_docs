# unreal.CommonBoundActionButton

```python
class unreal.CommonBoundActionButton(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``CommonButtonBase``


Common Bound Action Button

**C++ Source:**

- **Plugin**: CommonUI

- **Module**: CommonUI

- **File**: CommonBoundActionButton.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `accessible_behavior` (SlateAccessibleBehavior): [Read-Write] Whether or not the widget is accessible, and how to describe it. If set to custom, additional customization options will appear.

- `accessible_summary_behavior` (SlateAccessibleBehavior): [Read-Write] How to describe this widget when it’s being presented through a summary of a parent widget. If set to custom, additional customization options will appear.

- `accessible_summary_text` (Text): [Read-Write] When AccessibleSummaryBehavior is set to Custom, this is the text that will be used to describe the widget.

- `accessible_text` (Text): [Read-Write] When AccessibleBehavior is set to Custom, this is the text that will be used to describe the widget.

- `apply_alpha_on_disable` (bool): [Read-Write] The type of mouse action required by the user to trigger the button’s ‘Click’

- `can_children_be_accessible` (bool): [Read-Write] Whether or not children of this widget can appear as distinct accessible widgets.

- `click_event` (WidgetEventField): [Read-Write]

- `click_method` (ButtonClickMethod): [Read-Write] The type of mouse action required by the user to trigger the button’s ‘Click’

- `clicked_slate_sound_override` (SlateSound): [Read-Write] Optional override for the sound to play when this button is clicked (based on Click/Touch/Press methods).

- `clipping` (WidgetClipping): [Read-Write] Controls how the clipping behavior of this widget. Normally content that overflows the
bounds of the widget continues rendering. Enabling clipping prevents that overflowing content
from being seen.

NOTE: Elements in different clipping spaces can not be batched together, and so there is a
performance cost to clipping. Do not enable clipping unless a panel actually needs to prevent
content from showing up outside its bounds.

- `color_and_opacity` (LinearColor): [Read-Write] The color and opacity of this widget. Tints all child widgets.

- `consume_pointer_input` (bool): [Read-Write] Set this to true if you don’t want any pointer (mouse and touch) input to bubble past this widget

- `cursor` (MouseCursor): [Read-Write] The cursor to show when the mouse is over the widget

- `desired_focus_widget` (WidgetChild): [Read-Write]

- `display_in_action_bar` (bool): [Read-Write] True to generally display this widget’s actions in the action bar, assuming it has actions.

- `display_input_action_when_not_interactable` (bool): [Read-Write] True if the input action should be displayed when the button is not interactable

- `flow_direction_preference` (FlowDirectionPreference): [Read-Write] Allows you to set a new flow direction

- `foreground_color` (SlateColor): [Read-Write] The foreground color of the widget, this is inherited by sub widgets. Any color property
that is marked as inherit will use this color.

- `hide_input_action` (bool): [Read-Write] Whether to hide the input action widget at all times (useful for textless small buttons)

- `hide_input_action_with_keyboard` (bool): [Read-Write] True if the input action should be hidden while the user is using a keyboard

- `hold_data` (type(Class)): [Read-Write] Press and Hold values used for Keyboard and Mouse, Gamepad and Touch, depending on the current input type

- `hovered_slate_sound_override` (SlateSound): [Read-Write] Optional override for the sound to play when this button is hovered.
Also used for the Selected and Locked Hovered state if their respective overrides are empty.

- `input_action_widget` (CommonActionWidget): [Read-Write] Optionally bound widget for visualization behavior of an input action;
NOTE: If specified, will visualize according to the following algorithm:
If TriggeringEnhancedInputAction is specified, visualize it else:
If TriggeringInputAction is specified, visualize it else:
If TriggeredInputAction is specified, visualize it else:
Visualize the default click action while hovered

- `input_mode_override` (CommonInputMode): [Read-Write] Set this to Game for special cases where an input action needs to be set for an in-game button.

- `input_priority` (int32): [Read-Write] This is the priority for the TriggeringInputAction. The first, HIGHEST PRIORITY widget will handle the input action, and no other widgets will be considered.
Additionally, no inputs with a priority below the current ActivatablePanel’s Input Priority value will even be considered!
TODO:: This is part of legacy CommonUI and should be removed

- `interactable_when_selected` (bool): [Read-Write] If true, the button may be clicked while selected. Otherwise, interaction is disabled in the selected state.

- `is_enabled` (bool): [Read-Write] Sets whether this widget can be modified interactively by the user

- `is_focusable` (bool): [Read-Write] Setting this flag to true, allows this widget to accept focus when clicked, or when navigated to.

- `is_persistent_binding` (bool): [Read-Write] DANGER! Be very, very careful with this. Unless you absolutely know what you’re doing, this is not the property you’re looking for.

True to register the action bound to this button as a “persistent” binding. False (default) will register a standard activation-based binding.
A persistent binding ignores the standard ruleset for UI input routing - the binding will be live immediately upon construction of the button.

- `is_volatile` (bool): [Read-Write] If true prevents the widget or its child’s geometry or layout information from being cached. If this widget
changes every frame, but you want it to still be in an invalidation panel you should make it as volatile
instead of invalidating it every frame, which would prevent the invalidation panel from actually
ever caching anything.

- `link_requires_hold_to_binding_hold` (bool): [Read-Write] Set to true if clicking this button should require holding it when the bound action is a hold action

- `locked` (bool): [Read-Write] True if this button is currently locked.
Locked button can be hovered, focused, and pressed, but the Click event will not go through.
Business logic behind it will not be executed. Designed for progressive disclosure

- `locked_clicked_slate_sound_override` (SlateSound): [Read-Write] Optional override for the sound to play when this button is clicked while Locked

- `locked_hovered_slate_sound_override` (SlateSound): [Read-Write] Optional override for the sound to play when this button is hovered while Locked

- `locked_pressed_slate_sound_override` (SlateSound): [Read-Write] Optional override for the sound to play when this button is pressed while Locked

- `max_height` (int32): [Read-Write] The maximum height of the button (only used if greater than the style’s maximum)

- `max_width` (int32): [Read-Write] The maximum width of the button (only used if greater than the style’s maximum)

- `min_height` (int32): [Read-Write] The minimum height of the button (only used if greater than the style’s minimum)

- `min_width` (int32): [Read-Write] The minimum width of the button (only used if greater than the style’s minimum)

- `navigate_to_next_widget_on_disable` (bool): [Read-Write] If this button is currently in focus, and is disabled, hidden, or collapsed then focus will be routed to the next available widget

- `navigation` (WidgetNavigation): [Read-Write] The navigation object for this widget is optionally created if the user has configured custom
navigation rules for this widget in the widget designer. Those rules determine how navigation transitions
can occur between widgets.

- `on_button_base_clicked` (CommonButtonBaseClicked): [Read-Write]

- `on_button_base_double_clicked` (CommonButtonBaseClicked): [Read-Write]

- `on_button_base_drag_detected` (OnButtonBaseGeoOperationDynamic): [Read-Write]

- `on_button_base_drag_enter` (OnButtonBaseGeoOperationDynamic): [Read-Write]

- `on_button_base_drag_leave` (OnButtonBaseOperationDynamic): [Read-Write]

- `on_button_base_drag_over` (OnButtonBaseGeoOperationDynamic): [Read-Write]

- `on_button_base_drop` (OnButtonBaseGeoOperationDynamic): [Read-Write]

- `on_button_base_focused` (CommonButtonBaseClicked): [Read-Write]

- `on_button_base_hovered` (CommonButtonBaseClicked): [Read-Write]

- `on_button_base_lock_clicked` (CommonButtonBaseClicked): [Read-Write]

- `on_button_base_lock_double_clicked` (CommonButtonBaseClicked): [Read-Write]

- `on_button_base_selected` (CommonButtonBaseClicked): [Read-Write]

- `on_button_base_unfocused` (CommonButtonBaseClicked): [Read-Write]

- `on_button_base_unhovered` (CommonButtonBaseClicked): [Read-Write]

- `on_button_base_unselected` (CommonButtonBaseClicked): [Read-Write]

- `on_selected_changed_base` (CommonSelectedStateChangedBase): [Read-Write]

- `on_visibility_changed` (OnVisibilityChangedEvent): [Read-Write] Called when the visibility has changed

- `override_accessible_defaults` (bool): [Read-Write] Override all of the default accessibility behavior and text for this widget.

- `override_cursor` (bool): [Read-Write]

- `padding` (Margin): [Read-Write] The padding area around the content.

- `pixel_snapping` (WidgetPixelSnapping): [Read-Write] If the widget will draw snapped to the nearest pixel. Improves clarity but might cause visibile stepping in animation

- `press_method` (ButtonPressMethod): [Read-Write]

- `pressed_slate_sound_override` (SlateSound): [Read-Write] Optional override for the sound to play when this button is pressed.
Also used for the Selected and Locked Pressed state if their respective overrides are empty.

- `preview_background` (Texture2D): [Read-Write] A preview background that you can use when designing the UI to get a sense of scale on the screen. Use
a texture with a screenshot of your game in it, for example if you were designing a HUD.

- `priority` (int32): [Read-Write]

- `render_opacity` (float): [Read-Write] The opacity of the widget

- `render_transform` (WidgetTransform): [Read-Write] The render transform of the widget allows for arbitrary 2D transforms to be applied to the widget.

- `render_transform_pivot` (Vector2D): [Read-Write] The render transform pivot controls the location about which transforms are applied.
This value is a normalized coordinate about which things like rotations will occur.

- `requires_hold` (bool): [Read-Write] True if this button should have a press and hold behavior, triggering the click when the specified hold time is met

- `selectable` (bool): [Read-Write] True if the button supports being in a “selected” state, which will update the style accordingly

- `selected_clicked_slate_sound_override` (SlateSound): [Read-Write] Optional override for the sound to play when this button is clicked while Selected

- `selected_hovered_slate_sound_override` (SlateSound): [Read-Write] Optional override for the sound to play when this button is hovered while Selected

- `selected_pressed_slate_sound_override` (SlateSound): [Read-Write] Optional override for the sound to play when this button is pressed while Selected

- `should_select_upon_receiving_focus` (bool): [Read-Write] If true, the button will be selected when it receives focus.

- `should_use_fallback_default_input_action` (bool): [Read-Write] True if this button should use the default fallback input action (bool is useful for buttons that shouldn’t because they are never directly hit via controller)

- `simulate_hover_on_touch_input` (bool): [Read-Write] True if this button should play the hover effect when pressed by a touch input

- `slot` (PanelSlot): [Read-Write] The parent slot of the UWidget. Allows us to easily inline edit the layout controlling this widget.

- `stop_action` (bool): [Read-Write]

- `style` (type(Class)): [Read-Write] References the button style asset that defines a style in multiple sizes

- `text_action_name` (CommonTextBlock): [Read-Write]

- `tick_frequency` (WidgetTickFrequency): [Read-Write] This widget is allowed to tick. If this is unchecked tick will never be called, animations will not play correctly, and latent actions will not execute.
Uncheck this for performance reasons only

- `toggleable` (bool): [Read-Write] True if the button can be deselected by clicking it when selected

- `tool_tip_text` (Text): [Read-Write] Tooltip text to show when the user hovers over the widget with the mouse

- `tool_tip_widget` (Widget): [Read-Only] Tooltip widget to show when the user hovers over the widget with the mouse

- `touch_method` (ButtonTouchMethod): [Read-Write]

- `trigger_clicked_after_selection` (bool): [Read-Write]

- `triggering_enhanced_input_action` (InputAction): [Read-Write] The enhanced input action that is bound to this button. The common input manager will trigger this button to
click if the action was pressed

- `triggering_input_action` (DataTableRowHandle): [Read-Write] The input action that is bound to this button. The common input manager will trigger this button to
click if the action was pressed

- `visibility` (SlateVisibility): [Read-Write] The visibility of the widget



---

_property_ `link_requires_hold_to_binding_hold`: bool

[Read-Only] Set to true if clicking this button should require holding it when the bound action is a hold action

**Type:**

( bool)


---

**on_update_input_action**() → `None`

On Update Input Action


---

_property_ `text_action_name`: CommonTextBlock

[Read-Only]

**Type:**

( CommonTextBlock)

### Table of Contents

- `unreal.CommonBoundActionButton`
  - `CommonBoundActionButton`
    - `CommonBoundActionButton.link_requires_hold_to_binding_hold`
    - `CommonBoundActionButton.on_update_input_action()`
    - `CommonBoundActionButton.text_action_name`
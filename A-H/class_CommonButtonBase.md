# unreal.CommonButtonBase

```python
class unreal.CommonButtonBase(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``CommonUserWidget``


Button that disables itself when not active. Also updates actions for CommonActionWidget if bound to display platform-specific icons.

**C++ Source:**

- **Plugin**: CommonUI

- **Module**: CommonUI

- **File**: CommonButtonBase.h


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

_property_ `apply_alpha_on_disable`: bool

[Read-Only] The type of mouse action required by the user to trigger the button’s ‘Click’

**Type:**

( bool)


---

**bp_on_clicked**() → `None`

BP on Clicked


---

**bp_on_deselected**() → `None`

BP on Deselected


---

**bp_on_disabled**() → `None`

BP on Disabled


---

**bp_on_double_clicked**() → `None`

BP on Double Clicked


---

**bp_on_enabled**() → `None`

BP on Enabled


---

**bp_on_focus_lost**() → `None`

BP on Focus Lost


---

**bp_on_focus_received**() → `None`

BP on Focus Received


---

**bp_on_hovered**() → `None`

BP on Hovered


---

**bp_on_input_action_triggered**() → `None`

BP on Input Action Triggered


---

**bp_on_input_method_changed**( _current_input_type_) → `None`

BP on Input Method Changed

Parameters:

**current\_input\_type** ( _CommonInputType_)


---

**bp_on_lock_clicked**() → `None`

BP on Lock Clicked


---

**bp_on_lock_double_clicked**() → `None`

BP on Lock Double Clicked


---

**bp_on_locked_changed**( _is_locked_) → `None`

BP on Locked Changed

Parameters:

**is\_locked** ( _bool_)


---

**bp_on_pressed**() → `None`

BP on Pressed


---

**bp_on_released**() → `None`

BP on Released


---

**bp_on_requires_hold_changed**() → `None`

BP on Requires Hold Changed


---

**bp_on_selected**() → `None`

BP on Selected


---

**bp_on_unhovered**() → `None`

BP on Unhovered


---

**clear_selection**() → `None`

Clear Selection


---

_property_ `click_event`: WidgetEventField

[Read-Only]

**Type:**

( WidgetEventField)


---

_property_ `click_method`: ButtonClickMethod

[Read-Only] The type of mouse action required by the user to trigger the button’s ‘Click’

**Type:**

( ButtonClickMethod)


---

_property_ `clicked_slate_sound_override`: SlateSound

[Read-Only] Optional override for the sound to play when this button is clicked (based on Click/Touch/Press methods).

**Type:**

( SlateSound)


---

**disable_button_with_reason**( _disabled_reason_) → `None`

Disables this button with a reason (use instead of SetIsEnabled)

Parameters:

**disabled\_reason** ( _Text_)


---

_property_ `display_input_action_when_not_interactable`: bool

[Read-Only] True if the input action should be displayed when the button is not interactable

**Type:**

( bool)


---

**get_current_button_padding**() → `MarginReturns:`

out\_button\_padding (Margin):

Return type:

Margin


---

**get_current_custom_padding**() → `MarginReturns:`

out\_custom\_padding (Margin):

Return type:

Margin


---

**get_current_text_style**() → `CommonTextStyleReturns:`

The text style that corresponds to the current size and selection state

Return type:

CommonTextStyle

get\_current\_text\_style\_class()Returns:

The class of the text style that corresponds to the current size and selection state

Return type:

type( Class)


---

**get_enhanced_input_action**() → `InputAction`

Gets the appropriate enhanced input action that is set

Return type:

InputAction


---

**get_input_action**() → `DataTableRowHandleorNone`

Gets the appropriate input action that is set

Returns:

input\_action\_row (DataTableRowHandle):

Return type:

DataTableRowHandle or None


---

**get_is_focusable**() → `bool`

Gets the bIsFocusable flag

Return type:

bool


---

**get_locked**() → `boolReturns:`

True if the button is currently locked, False otherwise

Return type:

bool


---

**get_required_hold_time**() → `float`

Returns required hold time for performing a triggering action.

Return type:

float


---

**get_requires_hold**() → `bool`

Returns true if this button has a hold behavior, even if the triggering action is not holdable.

Return type:

bool


---

**get_selected**() → `boolReturns:`

True if the button is currently in a selected state, False otherwise

Return type:

bool


---

**get_should_select_upon_receiving_focus**() → `bool`

Get whether the button should become selected upon receiving focus or not

Return type:

bool


---

**get_single_material_style_mid**() → `MaterialInstanceDynamic`

Returns the dynamic instance of the material being used for this button, if it is using a single material style.

Return type:

MaterialInstanceDynamic


---

**get_style**() → `CommonButtonStyleReturns:`

Current button style

Return type:

CommonButtonStyle


---

_property_ `hide_input_action`: bool

[Read-Only] Whether to hide the input action widget at all times (useful for textless small buttons)

**Type:**

( bool)


---

_property_ `hide_input_action_with_keyboard`: bool

[Read-Only] True if the input action should be hidden while the user is using a keyboard

**Type:**

( bool)


---

_property_ `hold_data`: Class

[Read-Only] Press and Hold values used for Keyboard and Mouse, Gamepad and Touch, depending on the current input type

**Type:**

( type( Class))


---

_property_ `hovered_slate_sound_override`: SlateSound

[Read-Only] Optional override for the sound to play when this button is hovered.
Also used for the Selected and Locked Hovered state if their respective overrides are empty.

**Type:**

( SlateSound)


---

_property_ `input_action_widget`: CommonActionWidget

[Read-Only] Optionally bound widget for visualization behavior of an input action;
NOTE: If specified, will visualize according to the following algorithm:
If TriggeringEnhancedInputAction is specified, visualize it else:
If TriggeringInputAction is specified, visualize it else:
If TriggeredInputAction is specified, visualize it else:
Visualize the default click action while hovered

**Type:**

( CommonActionWidget)


---

_property_ `input_priority`: int

[Read-Only] This is the priority for the TriggeringInputAction. The first, HIGHEST PRIORITY widget will handle the input action, and no other widgets will be considered.
Additionally, no inputs with a priority below the current ActivatablePanel’s Input Priority value will even be considered!
TODO:: This is part of legacy CommonUI and should be removed

**Type:**

(int32)


---

_property_ `interactable_when_selected`: bool

[Read-Only] If true, the button may be clicked while selected. Otherwise, interaction is disabled in the selected state.

**Type:**

( bool)


---

**is_interaction_enabled**() → `bool`

Is this button currently interactable? (use instead of GetIsEnabled)

Return type:

bool


---

**is_pressed**() → `bool`

Is this button currently pressed?

Return type:

bool


---

_property_ `locked`: bool

[Read-Only] True if this button is currently locked.
Locked button can be hovered, focused, and pressed, but the Click event will not go through.
Business logic behind it will not be executed. Designed for progressive disclosure

**Type:**

( bool)


---

_property_ `locked_clicked_slate_sound_override`: SlateSound

[Read-Only] Optional override for the sound to play when this button is clicked while Locked

**Type:**

( SlateSound)


---

_property_ `locked_hovered_slate_sound_override`: SlateSound

[Read-Only] Optional override for the sound to play when this button is hovered while Locked

**Type:**

( SlateSound)


---

_property_ `locked_pressed_slate_sound_override`: SlateSound

[Read-Only] Optional override for the sound to play when this button is pressed while Locked

**Type:**

( SlateSound)


---

_property_ `max_height`: int

[Read-Only] The maximum height of the button (only used if greater than the style’s maximum)

**Type:**

(int32)


---

_property_ `max_width`: int

[Read-Only] The maximum width of the button (only used if greater than the style’s maximum)

**Type:**

(int32)


---

_property_ `min_height`: int

[Read-Only] The minimum height of the button (only used if greater than the style’s minimum)

**Type:**

(int32)


---

_property_ `min_width`: int

[Read-Only] The minimum width of the button (only used if greater than the style’s minimum)

**Type:**

(int32)


---

_property_ `navigate_to_next_widget_on_disable`: bool

[Read-Only] If this button is currently in focus, and is disabled, hidden, or collapsed then focus will be routed to the next available widget

**Type:**

( bool)


---

**on_action_complete**() → `None`

Callback fired when hold events complete


---

**on_action_progress**( _held_percent_) → `None`

Callback fired continously during hold interactions

Parameters:

**held\_percent** ( _float_)


---

_property_ `on_button_base_clicked`: CommonButtonBaseClicked

[Read-Write]

**Type:**

( CommonButtonBaseClicked)


---

_property_ `on_button_base_double_clicked`: CommonButtonBaseClicked

[Read-Write]

**Type:**

( CommonButtonBaseClicked)


---

_property_ `on_button_base_drag_detected`: OnButtonBaseGeoOperationDynamic

[Read-Write]

**Type:**

( OnButtonBaseGeoOperationDynamic)


---

_property_ `on_button_base_drag_enter`: OnButtonBaseGeoOperationDynamic

[Read-Write]

**Type:**

( OnButtonBaseGeoOperationDynamic)


---

_property_ `on_button_base_drag_leave`: OnButtonBaseOperationDynamic

[Read-Write]

**Type:**

( OnButtonBaseOperationDynamic)


---

_property_ `on_button_base_drag_over`: OnButtonBaseGeoOperationDynamic

[Read-Write]

**Type:**

( OnButtonBaseGeoOperationDynamic)


---

_property_ `on_button_base_drop`: OnButtonBaseGeoOperationDynamic

[Read-Write]

**Type:**

( OnButtonBaseGeoOperationDynamic)


---

_property_ `on_button_base_focused`: CommonButtonBaseClicked

[Read-Write]

**Type:**

( CommonButtonBaseClicked)


---

_property_ `on_button_base_hovered`: CommonButtonBaseClicked

[Read-Write]

**Type:**

( CommonButtonBaseClicked)


---

_property_ `on_button_base_lock_clicked`: CommonButtonBaseClicked

[Read-Write]

**Type:**

( CommonButtonBaseClicked)


---

_property_ `on_button_base_lock_double_clicked`: CommonButtonBaseClicked

[Read-Write]

**Type:**

( CommonButtonBaseClicked)


---

_property_ `on_button_base_selected`: CommonButtonBaseClicked

[Read-Write]

**Type:**

( CommonButtonBaseClicked)


---

_property_ `on_button_base_unfocused`: CommonButtonBaseClicked

[Read-Write]

**Type:**

( CommonButtonBaseClicked)


---

_property_ `on_button_base_unhovered`: CommonButtonBaseClicked

[Read-Write]

**Type:**

( CommonButtonBaseClicked)


---

_property_ `on_button_base_unselected`: CommonButtonBaseClicked

[Read-Write]

**Type:**

( CommonButtonBaseClicked)


---

**on_current_text_style_changed**() → `None`

Allows derived classes to take action when the current text style has changed


---

_property_ `on_selected_changed_base`: CommonSelectedStateChangedBase

[Read-Write]

**Type:**

( CommonSelectedStateChangedBase)


---

**on_triggered_input_action_changed**( _new_triggered_action_) → `None`

Callback fired when input action datatable row changes

Parameters:

**new\_triggered\_action** ( _DataTableRowHandle_)


---

**on_triggering_enhanced_input_action_changed**( _input_action_) → `None`

Callback fired when enhanced input action changes

Parameters:

**input\_action** ( _InputAction_)


---

**on_triggering_input_action_changed**( _new_triggered_action_) → `None`

Callback fired when triggered input action datatable row changes

Parameters:

**new\_triggered\_action** ( _DataTableRowHandle_)


---

_property_ `press_method`: ButtonPressMethod

[Read-Only]

**Type:**

( ButtonPressMethod)


---

_property_ `pressed_slate_sound_override`: SlateSound

[Read-Only] Optional override for the sound to play when this button is pressed.
Also used for the Selected and Locked Pressed state if their respective overrides are empty.

**Type:**

( SlateSound)


---

_property_ `requires_hold`: bool

[Read-Only] True if this button should have a press and hold behavior, triggering the click when the specified hold time is met

**Type:**

( bool)


---

_property_ `selectable`: bool

[Read-Only] True if the button supports being in a “selected” state, which will update the style accordingly

**Type:**

( bool)


---

_property_ `selected_clicked_slate_sound_override`: SlateSound

[Read-Only] Optional override for the sound to play when this button is clicked while Selected

**Type:**

( SlateSound)


---

_property_ `selected_hovered_slate_sound_override`: SlateSound

[Read-Only] Optional override for the sound to play when this button is hovered while Selected

**Type:**

( SlateSound)


---

_property_ `selected_pressed_slate_sound_override`: SlateSound

[Read-Only] Optional override for the sound to play when this button is pressed while Selected

**Type:**

( SlateSound)


---

**set_allow_drag_drop**( _allow_drag_drop_) → `None`

Updates the bAllowDragDrop flag on the RootButton

Parameters:

**allow\_drag\_drop** ( _bool_)


---

**set_click_method**( _click_method_) → `None`

Set the click method for mouse interaction

Parameters:

**click\_method** ( _ButtonClickMethod_)


---

**set_clicked_sound_override**( _sound_) → `None`

Set Clicked Sound Override

Parameters:

**sound** ( _SoundBase_)


---

**set_hide_input_action**( _hide_input_action_) → `None`

Set Hide Input Action

Parameters:

**hide\_input\_action** ( _bool_)


---

**set_hovered_sound_override**( _sound_) → `None`

Set Hovered Sound Override

Parameters:

**sound** ( _SoundBase_)


---

**set_input_action_progress_material**( _progress_material_brush_, _progress_material_param_) → `None`

Set Input Action Progress Material

Parameters:

- **progress\_material\_brush** ( _SlateBrush_)

- **progress\_material\_param** ( _Name_)



---

**set_is_focusable**( _is_focusable_) → `None`

Updates the bIsFocusable flag

Parameters:

**is\_focusable** ( _bool_)


---

**set_is_interactable_when_selected**( _interactable_when_selected_) → `None`

Change whether this widget is selectable at all. If false and currently selected, will deselect.

Parameters:

**interactable\_when\_selected** ( _bool_)


---

**set_is_interaction_enabled**( _is_interaction_enabled_) → `None`

Change whether this widget is selectable at all. If false and currently selected, will deselect.

Parameters:

**is\_interaction\_enabled** ( _bool_)


---

**set_is_locked**( _is_locked_) → `None`

Change whether this widget is locked. If locked, the button can be focusable and responsive to mouse input but will not broadcast OnClicked events.

Parameters:

**is\_locked** ( _bool_)


---

**set_is_selectable**( _is_selectable_) → `None`

Change whether this widget is selectable at all. If false and currently selected, will deselect.

Parameters:

**is\_selectable** ( _bool_)


---

**set_is_selected**( _selected_, _give_click_feedback=True_) → `None`

Change the selected state manually.

Parameters:

- **selected** ( _bool_)

- **give\_click\_feedback** ( _bool_) – If true, the button may give user feedback as if it were clicked. IE: Play a click sound, trigger animations as if it were clicked.



---

**set_is_toggleable**( _is_toggleable_) → `None`

Change whether this widget is toggleable. If toggleable, clicking when selected will deselect.

Parameters:

**is\_toggleable** ( _bool_)


---

**set_locked_clicked_sound_override**( _sound_) → `None`

Set Locked Clicked Sound Override

Parameters:

**sound** ( _SoundBase_)


---

**set_locked_hovered_sound_override**( _sound_) → `None`

Set Locked Hovered Sound Override

Parameters:

**sound** ( _SoundBase_)


---

**set_locked_pressed_sound_override**( _sound_) → `None`

Set Locked Pressed Sound Override

Parameters:

**sound** ( _SoundBase_)


---

**set_max_dimensions**( _max_width_, _max_height_) → `None`

Sets the maximum dimensions of this button

Parameters:

- **max\_width** ( _int32_)

- **max\_height** ( _int32_)



---

**set_min_dimensions**( _min_width_, _min_height_) → `None`

Sets the minimum dimensions of this button

Parameters:

- **min\_width** ( _int32_)

- **min\_height** ( _int32_)



---

**set_press_method**( _press_method_) → `None`

Set the click method for keyboard/gamepad button press interaction

Parameters:

**press\_method** ( _ButtonPressMethod_)


---

**set_pressed_sound_override**( _sound_) → `None`

Set Pressed Sound Override

Parameters:

**sound** ( _SoundBase_)


---

**set_requires_hold**( _requires_hold_) → `None`

Change whether this button should have a hold behavior even if the triggering action is not holdable.

Parameters:

**requires\_hold** ( _bool_)


---

**set_selected_clicked_sound_override**( _sound_) → `None`

Set Selected Clicked Sound Override

Parameters:

**sound** ( _SoundBase_)


---

**set_selected_hovered_sound_override**( _sound_) → `None`

Set Selected Hovered Sound Override

Parameters:

**sound** ( _SoundBase_)


---

**set_selected_internal**( _selected_, _allow_sound=True_, _broadcast=True_) → `None`

Internal method to allow the selected state to be set regardless of selectability or toggleability

Parameters:

- **selected** ( _bool_)

- **allow\_sound** ( _bool_)

- **broadcast** ( _bool_)



---

**set_selected_pressed_sound_override**( _sound_) → `None`

Set Selected Pressed Sound Override

Parameters:

**sound** ( _SoundBase_)


---

**set_should_select_upon_receiving_focus**( _should_select_upon_receiving_focus_) → `None`

Set whether the button should become selected upon receiving focus or not; Only settable for buttons that are selectable

Parameters:

**should\_select\_upon\_receiving\_focus** ( _bool_)


---

**set_should_use_fallback_default_input_action**( _should_use_fallback_default_input_action_) → `None`

Change whether this widget should use the fallback default input action.

Parameters:

**should\_use\_fallback\_default\_input\_action** ( _bool_)


---

**set_style**( _style=None_) → `None`

Sets the style of this button, rebuilds the internal styling

Parameters:

**style** ( _type_ _(_ _Class_ _)_)


---

**set_touch_method**( _touch_method_) → `None`

Set the click method for touch interaction

Parameters:

**touch\_method** ( _ButtonTouchMethod_)


---

**set_triggered_input_action**( _input_action_row_) → `None`

Updates the current triggered action

Parameters:

**input\_action\_row** ( _DataTableRowHandle_)


---

**set_triggering_enhanced_input_action**( _input_action_) → `None`

Updates the current triggering enhanced input action, requires enhanced input enabled in CommonUI settings

Parameters:

**input\_action** ( _InputAction_)


---

**set_triggering_input_action**( _input_action_row_) → `None`

Updates the current triggering action

Parameters:

**input\_action\_row** ( _DataTableRowHandle_)


---

_property_ `should_select_upon_receiving_focus`: bool

[Read-Only] If true, the button will be selected when it receives focus.

**Type:**

( bool)


---

_property_ `should_use_fallback_default_input_action`: bool

[Read-Only] True if this button should use the default fallback input action (bool is useful for buttons that shouldn’t because they are never directly hit via controller)

**Type:**

( bool)


---

_property_ `simulate_hover_on_touch_input`: bool

[Read-Only] True if this button should play the hover effect when pressed by a touch input

**Type:**

( bool)


---

**stop_double_click_propagation**() → `None`

Unless this is called, we will assume the double click should be converted into a normal click.


---

_property_ `style`: Class

[Read-Only] References the button style asset that defines a style in multiple sizes

**Type:**

( type( Class))


---

_property_ `toggleable`: bool

[Read-Only] True if the button can be deselected by clicking it when selected

**Type:**

( bool)


---

_property_ `touch_method`: ButtonTouchMethod

[Read-Only]

**Type:**

( ButtonTouchMethod)


---

_property_ `trigger_clicked_after_selection`: bool

[Read-Only]

**Type:**

( bool)


---

_property_ `triggering_enhanced_input_action`: InputAction

[Read-Only] The enhanced input action that is bound to this button. The common input manager will trigger this button to
click if the action was pressed

**Type:**

( InputAction)


---

_property_ `triggering_input_action`: DataTableRowHandle

[Read-Only] The input action that is bound to this button. The common input manager will trigger this button to
click if the action was pressed

**Type:**

( DataTableRowHandle)

### Table of Contents

- `unreal.CommonButtonBase`
  - `CommonButtonBase`
    - `CommonButtonBase.apply_alpha_on_disable`
    - `CommonButtonBase.bp_on_clicked()`
    - `CommonButtonBase.bp_on_deselected()`
    - `CommonButtonBase.bp_on_disabled()`
    - `CommonButtonBase.bp_on_double_clicked()`
    - `CommonButtonBase.bp_on_enabled()`
    - `CommonButtonBase.bp_on_focus_lost()`
    - `CommonButtonBase.bp_on_focus_received()`
    - `CommonButtonBase.bp_on_hovered()`
    - `CommonButtonBase.bp_on_input_action_triggered()`
    - `CommonButtonBase.bp_on_input_method_changed()`
    - `CommonButtonBase.bp_on_lock_clicked()`
    - `CommonButtonBase.bp_on_lock_double_clicked()`
    - `CommonButtonBase.bp_on_locked_changed()`
    - `CommonButtonBase.bp_on_pressed()`
    - `CommonButtonBase.bp_on_released()`
    - `CommonButtonBase.bp_on_requires_hold_changed()`
    - `CommonButtonBase.bp_on_selected()`
    - `CommonButtonBase.bp_on_unhovered()`
    - `CommonButtonBase.clear_selection()`
    - `CommonButtonBase.click_event`
    - `CommonButtonBase.click_method`
    - `CommonButtonBase.clicked_slate_sound_override`
    - `CommonButtonBase.disable_button_with_reason()`
    - `CommonButtonBase.display_input_action_when_not_interactable`
    - `CommonButtonBase.get_current_button_padding()`
    - `CommonButtonBase.get_current_custom_padding()`
    - `CommonButtonBase.get_current_text_style()`
    - `CommonButtonBase.get_current_text_style_class()`
    - `CommonButtonBase.get_enhanced_input_action()`
    - `CommonButtonBase.get_input_action()`
    - `CommonButtonBase.get_is_focusable()`
    - `CommonButtonBase.get_locked()`
    - `CommonButtonBase.get_required_hold_time()`
    - `CommonButtonBase.get_requires_hold()`
    - `CommonButtonBase.get_selected()`
    - `CommonButtonBase.get_should_select_upon_receiving_focus()`
    - `CommonButtonBase.get_single_material_style_mid()`
    - `CommonButtonBase.get_style()`
    - `CommonButtonBase.hide_input_action`
    - `CommonButtonBase.hide_input_action_with_keyboard`
    - `CommonButtonBase.hold_data`
    - `CommonButtonBase.hovered_slate_sound_override`
    - `CommonButtonBase.input_action_widget`
    - `CommonButtonBase.input_priority`
    - `CommonButtonBase.interactable_when_selected`
    - `CommonButtonBase.is_interaction_enabled()`
    - `CommonButtonBase.is_pressed()`
    - `CommonButtonBase.locked`
    - `CommonButtonBase.locked_clicked_slate_sound_override`
    - `CommonButtonBase.locked_hovered_slate_sound_override`
    - `CommonButtonBase.locked_pressed_slate_sound_override`
    - `CommonButtonBase.max_height`
    - `CommonButtonBase.max_width`
    - `CommonButtonBase.min_height`
    - `CommonButtonBase.min_width`
    - `CommonButtonBase.navigate_to_next_widget_on_disable`
    - `CommonButtonBase.on_action_complete()`
    - `CommonButtonBase.on_action_progress()`
    - `CommonButtonBase.on_button_base_clicked`
    - `CommonButtonBase.on_button_base_double_clicked`
    - `CommonButtonBase.on_button_base_drag_detected`
    - `CommonButtonBase.on_button_base_drag_enter`
    - `CommonButtonBase.on_button_base_drag_leave`
    - `CommonButtonBase.on_button_base_drag_over`
    - `CommonButtonBase.on_button_base_drop`
    - `CommonButtonBase.on_button_base_focused`
    - `CommonButtonBase.on_button_base_hovered`
    - `CommonButtonBase.on_button_base_lock_clicked`
    - `CommonButtonBase.on_button_base_lock_double_clicked`
    - `CommonButtonBase.on_button_base_selected`
    - `CommonButtonBase.on_button_base_unfocused`
    - `CommonButtonBase.on_button_base_unhovered`
    - `CommonButtonBase.on_button_base_unselected`
    - `CommonButtonBase.on_current_text_style_changed()`
    - `CommonButtonBase.on_selected_changed_base`
    - `CommonButtonBase.on_triggered_input_action_changed()`
    - `CommonButtonBase.on_triggering_enhanced_input_action_changed()`
    - `CommonButtonBase.on_triggering_input_action_changed()`
    - `CommonButtonBase.press_method`
    - `CommonButtonBase.pressed_slate_sound_override`
    - `CommonButtonBase.requires_hold`
    - `CommonButtonBase.selectable`
    - `CommonButtonBase.selected_clicked_slate_sound_override`
    - `CommonButtonBase.selected_hovered_slate_sound_override`
    - `CommonButtonBase.selected_pressed_slate_sound_override`
    - `CommonButtonBase.set_allow_drag_drop()`
    - `CommonButtonBase.set_click_method()`
    - `CommonButtonBase.set_clicked_sound_override()`
    - `CommonButtonBase.set_hide_input_action()`
    - `CommonButtonBase.set_hovered_sound_override()`
    - `CommonButtonBase.set_input_action_progress_material()`
    - `CommonButtonBase.set_is_focusable()`
    - `CommonButtonBase.set_is_interactable_when_selected()`
    - `CommonButtonBase.set_is_interaction_enabled()`
    - `CommonButtonBase.set_is_locked()`
    - `CommonButtonBase.set_is_selectable()`
    - `CommonButtonBase.set_is_selected()`
    - `CommonButtonBase.set_is_toggleable()`
    - `CommonButtonBase.set_locked_clicked_sound_override()`
    - `CommonButtonBase.set_locked_hovered_sound_override()`
    - `CommonButtonBase.set_locked_pressed_sound_override()`
    - `CommonButtonBase.set_max_dimensions()`
    - `CommonButtonBase.set_min_dimensions()`
    - `CommonButtonBase.set_press_method()`
    - `CommonButtonBase.set_pressed_sound_override()`
    - `CommonButtonBase.set_requires_hold()`
    - `CommonButtonBase.set_selected_clicked_sound_override()`
    - `CommonButtonBase.set_selected_hovered_sound_override()`
    - `CommonButtonBase.set_selected_internal()`
    - `CommonButtonBase.set_selected_pressed_sound_override()`
    - `CommonButtonBase.set_should_select_upon_receiving_focus()`
    - `CommonButtonBase.set_should_use_fallback_default_input_action()`
    - `CommonButtonBase.set_style()`
    - `CommonButtonBase.set_touch_method()`
    - `CommonButtonBase.set_triggered_input_action()`
    - `CommonButtonBase.set_triggering_enhanced_input_action()`
    - `CommonButtonBase.set_triggering_input_action()`
    - `CommonButtonBase.should_select_upon_receiving_focus`
    - `CommonButtonBase.should_use_fallback_default_input_action`
    - `CommonButtonBase.simulate_hover_on_touch_input`
    - `CommonButtonBase.stop_double_click_propagation()`
    - `CommonButtonBase.style`
    - `CommonButtonBase.toggleable`
    - `CommonButtonBase.touch_method`
    - `CommonButtonBase.trigger_clicked_after_selection`
    - `CommonButtonBase.triggering_enhanced_input_action`
    - `CommonButtonBase.triggering_input_action`
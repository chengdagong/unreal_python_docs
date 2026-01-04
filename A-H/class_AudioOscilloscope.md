# unreal.AudioOscilloscope

```python
class unreal.AudioOscilloscope(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Widget``


An oscilloscope UMG widget.

Supports displaying waveforms from incoming audio samples.

**C++ Source:**

- **Plugin**: AudioWidgets

- **Module**: AudioWidgets

- **File**: AudioOscilloscopeUMG.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `accessible_behavior` (SlateAccessibleBehavior): [Read-Write] Whether or not the widget is accessible, and how to describe it. If set to custom, additional customization options will appear.

- `accessible_summary_behavior` (SlateAccessibleBehavior): [Read-Write] How to describe this widget when it’s being presented through a summary of a parent widget. If set to custom, additional customization options will appear.

- `accessible_summary_text` (Text): [Read-Write] When AccessibleSummaryBehavior is set to Custom, this is the text that will be used to describe the widget.

- `accessible_text` (Text): [Read-Write] When AccessibleBehavior is set to Custom, this is the text that will be used to describe the widget.

- `amplitude_grid_labels_unit` (YAxisLabelsUnit): [Read-Write] Define the amplitude grid labels unit.

- `analysis_period_ms` (float): [Read-Write] The analysis period in milliseconds.

- `audio_bus` (AudioBus): [Read-Write] The audio bus used to obtain audio samples for the oscilloscope

- `can_children_be_accessible` (bool): [Read-Write] Whether or not children of this widget can appear as distinct accessible widgets.

- `channel_to_analyze` (int32): [Read-Write] The channel to analyze with the oscilloscope (only available if PanelLayoutType is set to “Advanced”).

- `clipping` (WidgetClipping): [Read-Write] Controls how the clipping behavior of this widget. Normally content that overflows the
bounds of the widget continues rendering. Enabling clipping prevents that overflowing content
from being seen.

NOTE: Elements in different clipping spaces can not be batched together, and so there is a
performance cost to clipping. Do not enable clipping unless a panel actually needs to prevent
content from showing up outside its bounds.

- `cursor` (MouseCursor): [Read-Write] The cursor to show when the mouse is over the widget

- `flow_direction_preference` (FlowDirectionPreference): [Read-Write] Allows you to set a new flow direction

- `is_enabled` (bool): [Read-Write] Sets whether this widget can be modified interactively by the user

- `is_volatile` (bool): [Read-Write] If true prevents the widget or its child’s geometry or layout information from being cached. If this widget
changes every frame, but you want it to still be in an invalidation panel you should make it as volatile
instead of invalidating it every frame, which would prevent the invalidation panel from actually
ever caching anything.

- `max_time_window_ms` (float): [Read-Write] The max time window in milliseconds.

- `navigation` (WidgetNavigation): [Read-Write] The navigation object for this widget is optionally created if the user has configured custom
navigation rules for this widget in the widget designer. Those rules determine how navigation transitions
can occur between widgets.

- `oscilloscope_style` (AudioOscilloscopePanelStyle): [Read-Write] The oscilloscope panel style

- `override_accessible_defaults` (bool): [Read-Write] Override all of the default accessibility behavior and text for this widget.

- `override_cursor` (bool): [Read-Write]

- `panel_layout_type` (AudioPanelLayoutType): [Read-Write] Show/Hide advanced panel layout.

- `pixel_snapping` (WidgetPixelSnapping): [Read-Write] If the widget will draw snapped to the nearest pixel. Improves clarity but might cause visibile stepping in animation

- `render_opacity` (float): [Read-Write] The opacity of the widget

- `render_transform` (WidgetTransform): [Read-Write] The render transform of the widget allows for arbitrary 2D transforms to be applied to the widget.

- `render_transform_pivot` (Vector2D): [Read-Write] The render transform pivot controls the location about which transforms are applied.
This value is a normalized coordinate about which things like rotations will occur.

- `show_amplitude_grid` (bool): [Read-Write] Show/Hide the amplitude grid.

- `show_amplitude_labels` (bool): [Read-Write] Show/Hide the amplitude labels.

- `show_time_grid` (bool): [Read-Write] Show/Hide the time grid.

- `slot` (PanelSlot): [Read-Write] The parent slot of the UWidget. Allows us to easily inline edit the layout controlling this widget.

- `time_grid_labels_unit` (XAxisLabelsUnit): [Read-Write] Define the time grid labels unit.

- `time_window_ms` (float): [Read-Write] The time window in milliseconds.

- `tool_tip_text` (Text): [Read-Write] Tooltip text to show when the user hovers over the widget with the mouse

- `tool_tip_widget` (Widget): [Read-Only] Tooltip widget to show when the user hovers over the widget with the mouse

- `trigger_mode` (AudioOscilloscopeTriggerMode): [Read-Write] The trigger detection behavior.

- `trigger_threshold` (float): [Read-Write] The trigger threshold position in the Y axis.

- `visibility` (SlateVisibility): [Read-Write] The visibility of the widget



---

_property_ `amplitude_grid_labels_unit`: YAxisLabelsUnit

[Read-Only] Define the amplitude grid labels unit.

**Type:**

( YAxisLabelsUnit)


---

_property_ `analysis_period_ms`: float

[Read-Only] The analysis period in milliseconds.

**Type:**

( float)


---

_property_ `audio_bus`: AudioBus

[Read-Only] The audio bus used to obtain audio samples for the oscilloscope

**Type:**

( AudioBus)


---

_property_ `channel_to_analyze`: int

[Read-Only] The channel to analyze with the oscilloscope (only available if PanelLayoutType is set to “Advanced”).

**Type:**

(int32)


---

_property_ `max_time_window_ms`: float

[Read-Only] The max time window in milliseconds.

**Type:**

( float)


---

_property_ `oscilloscope_style`: AudioOscilloscopePanelStyle

[Read-Only] The oscilloscope panel style

**Type:**

( AudioOscilloscopePanelStyle)


---

_property_ `panel_layout_type`: AudioPanelLayoutType

[Read-Only] Show/Hide advanced panel layout.

**Type:**

( AudioPanelLayoutType)


---

_property_ `show_amplitude_grid`: bool

[Read-Only] Show/Hide the amplitude grid.

**Type:**

( bool)


---

_property_ `show_amplitude_labels`: bool

[Read-Only] Show/Hide the amplitude labels.

**Type:**

( bool)


---

_property_ `show_time_grid`: bool

[Read-Only] Show/Hide the time grid.

**Type:**

( bool)


---

**start_processing**() → `None`

Starts the oscilloscope processing.


---

**stop_processing**() → `None`

Stops the oscilloscope processing.


---

_property_ `time_grid_labels_unit`: XAxisLabelsUnit

[Read-Only] Define the time grid labels unit.

**Type:**

( XAxisLabelsUnit)


---

_property_ `time_window_ms`: float

[Read-Only] The time window in milliseconds.

**Type:**

( float)


---

_property_ `trigger_mode`: AudioOscilloscopeTriggerMode

[Read-Only] The trigger detection behavior.

**Type:**

( AudioOscilloscopeTriggerMode)


---

_property_ `trigger_threshold`: float

[Read-Only] The trigger threshold position in the Y axis.

**Type:**

( float)

### Table of Contents

- `unreal.AudioOscilloscope`
  - `AudioOscilloscope`
    - `AudioOscilloscope.amplitude_grid_labels_unit`
    - `AudioOscilloscope.analysis_period_ms`
    - `AudioOscilloscope.audio_bus`
    - `AudioOscilloscope.channel_to_analyze`
    - `AudioOscilloscope.max_time_window_ms`
    - `AudioOscilloscope.oscilloscope_style`
    - `AudioOscilloscope.panel_layout_type`
    - `AudioOscilloscope.show_amplitude_grid`
    - `AudioOscilloscope.show_amplitude_labels`
    - `AudioOscilloscope.show_time_grid`
    - `AudioOscilloscope.start_processing()`
    - `AudioOscilloscope.stop_processing()`
    - `AudioOscilloscope.time_grid_labels_unit`
    - `AudioOscilloscope.time_window_ms`
    - `AudioOscilloscope.trigger_mode`
    - `AudioOscilloscope.trigger_threshold`
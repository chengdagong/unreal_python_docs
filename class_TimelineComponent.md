# unreal.TimelineComponent

```python
class unreal.TimelineComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``ActorComponent``


TimelineComponent holds a series of events, floats, vectors or colors with associated keyframes.
Events can be triggered at keyframes along the timeline.
Floats, vectors, and colors are interpolated between keyframes along the timeline.

**C++ Source:**

- **Module**: Engine

- **File**: TimelineComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!



---

**add_event**( _time_, _event_func_) → `None`

Add a callback event to the timeline

Parameters:

- **time** ( _float_)

- **event\_func** ( _OnTimelineEvent_)



---

**add_interp_float**( _float_curve_, _interp_func_, _property_name='None'_, _track_name='None'_) → `None`

Add a float interpolation to the timeline

Parameters:

- **float\_curve** ( _CurveFloat_)

- **interp\_func** ( _OnTimelineFloat_)

- **property\_name** ( _Name_)

- **track\_name** ( _Name_)



---

**add_interp_linear_color**( _linear_color_curve_, _interp_func_, _property_name='None'_, _track_name='None'_) → `None`

Add a linear color interpolation to the timeline

Parameters:

- **linear\_color\_curve** ( _CurveLinearColor_)

- **interp\_func** ( _OnTimelineLinearColor_)

- **property\_name** ( _Name_)

- **track\_name** ( _Name_)



---

**add_interp_vector**( _vector_curve_, _interp_func_, _property_name='None'_, _track_name='None'_) → `None`

Add a vector interpolation to the timeline

Parameters:

- **vector\_curve** ( _CurveVector_)

- **interp\_func** ( _OnTimelineVector_)

- **property\_name** ( _Name_)

- **track\_name** ( _Name_)



---

**get_ignore_time_dilation**() → `bool`

Get whether to ignore time dilation.

Return type:

bool


---

**get_play_rate**() → `float`

Get the current play rate for this timeline

Return type:

float


---

**get_playback_position**() → `float`

Get the current playback position of the Timeline

Return type:

float


---

**get_scaled_timeline_length**() → `float`

Get length of the timeline divided by the play rate

Return type:

float


---

**get_timeline_length**() → `float`

Get length of the timeline

Return type:

float


---

**is_looping**() → `bool`

Get whether we are looping or not

Return type:

bool


---

**is_playing**() → `bool`

Get whether this timeline is playing or not.

Return type:

bool


---

**is_reversing**() → `bool`

Get whether we are reversing or not

Return type:

bool


---

**play**() → `None`

Start playback of timeline


---

**play_from_start**() → `None`

Start playback of timeline from the start


---

**reverse**() → `None`

Start playback of timeline in reverse


---

**reverse_from_end**() → `None`

Start playback of timeline in reverse from the end


---

**set_float_curve**( _new_float_curve_, _float_track_name_) → `None`

Update a certain float track’s curve

Parameters:

- **new\_float\_curve** ( _CurveFloat_)

- **float\_track\_name** ( _Name_)



---

**set_ignore_time_dilation**( _new_ignore_time_dilation_) → `None`

Set whether to ignore time dilation.

Parameters:

**new\_ignore\_time\_dilation** ( _bool_)


---

**set_linear_color_curve**( _new_linear_color_curve_, _linear_color_track_name_) → `None`

Update a certain linear color track’s curve

Parameters:

- **new\_linear\_color\_curve** ( _CurveLinearColor_)

- **linear\_color\_track\_name** ( _Name_)



---

**set_looping**( _new_looping_) → `None`

true means we would loop, false means we should not.

Parameters:

**new\_looping** ( _bool_)


---

**set_new_time**( _new_time_) → `None`

Set the new playback position time to use

Parameters:

**new\_time** ( _float_)


---

**set_play_rate**( _new_rate_) → `None`

Sets the new play rate for this timeline

Parameters:

**new\_rate** ( _float_)


---

**set_playback_position**( _new_position_, _fire_events_, _fire_update=True_) → `None`

Jump to a position in the timeline.

Parameters:

- **new\_position** ( _float_)

- **fire\_events** ( _bool_) – If true, event functions that are between current position and new playback position will fire.

- **fire\_update** ( _bool_) – If true, the update output exec will fire after setting the new playback position.



---

**set_timeline_finished_func**( _new_timeline_finished_func_) → `None`

Set the delegate to call when timeline is finished

Parameters:

**new\_timeline\_finished\_func** ( _OnTimelineEvent_)


---

**set_timeline_length**( _new_length_) → `None`

Set length of the timeline

Parameters:

**new\_length** ( _float_)


---

**set_timeline_length_mode**( _new_length_mode_) → `None`

Sets the length mode of the timeline

Parameters:

**new\_length\_mode** ( _TimelineLengthMode_)


---

**set_timeline_post_update_func**( _new_timeline_post_update_func_) → `None`

Set the delegate to call after each timeline tick

Parameters:

**new\_timeline\_post\_update\_func** ( _OnTimelineEvent_)


---

**set_vector_curve**( _new_vector_curve_, _vector_track_name_) → `None`

Update a certain vector track’s curve

Parameters:

- **new\_vector\_curve** ( _CurveVector_)

- **vector\_track\_name** ( _Name_)



---

**stop**() → `None`

Stop playback of timeline

### Table of Contents

- `unreal.TimelineComponent`
  - `TimelineComponent`
    - `TimelineComponent.add_event()`
    - `TimelineComponent.add_interp_float()`
    - `TimelineComponent.add_interp_linear_color()`
    - `TimelineComponent.add_interp_vector()`
    - `TimelineComponent.get_ignore_time_dilation()`
    - `TimelineComponent.get_play_rate()`
    - `TimelineComponent.get_playback_position()`
    - `TimelineComponent.get_scaled_timeline_length()`
    - `TimelineComponent.get_timeline_length()`
    - `TimelineComponent.is_looping()`
    - `TimelineComponent.is_playing()`
    - `TimelineComponent.is_reversing()`
    - `TimelineComponent.play()`
    - `TimelineComponent.play_from_start()`
    - `TimelineComponent.reverse()`
    - `TimelineComponent.reverse_from_end()`
    - `TimelineComponent.set_float_curve()`
    - `TimelineComponent.set_ignore_time_dilation()`
    - `TimelineComponent.set_linear_color_curve()`
    - `TimelineComponent.set_looping()`
    - `TimelineComponent.set_new_time()`
    - `TimelineComponent.set_play_rate()`
    - `TimelineComponent.set_playback_position()`
    - `TimelineComponent.set_timeline_finished_func()`
    - `TimelineComponent.set_timeline_length()`
    - `TimelineComponent.set_timeline_length_mode()`
    - `TimelineComponent.set_timeline_post_update_func()`
    - `TimelineComponent.set_vector_curve()`
    - `TimelineComponent.stop()`
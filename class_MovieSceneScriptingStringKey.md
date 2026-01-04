# unreal.MovieSceneScriptingStringKey

```python
class unreal.MovieSceneScriptingStringKey(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MovieSceneScriptingKey``


Exposes a Sequencer string type key to Python/Blueprints.
Stores a reference to the data so changes to this class are forwarded onto the underlying data structures.

**C++ Source:**

- **Plugin**: SequencerScripting

- **Module**: SequencerScripting

- **File**: MovieSceneScriptingString.h



---

**get_time**( _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_) → `FrameTime`

Gets the time for this key from the owning channel.

Parameters:

**time\_unit** ( _MovieSceneTimeUnit_) – Should the time be returned in Display Rate frames (possibly with a sub-frame value) or in Tick Resolution with no sub-frame values?

Returns:

The time of this key which combines both the frame number and the sub-frame it is on. Sub-frame will be zero if you request Tick Resolution.

Return type:

FrameTime


---

**get_value**() → `str`

Gets the value for this key from the owning channel.

Returns:

The value for this key.

Return type:

str


---

**set_time**( _new_frame_number_, _sub_frame=0.000000_, _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_) → `None`

Sets the time for this key in the owning channel. Will replace any key that already exists at that frame number in this channel.

Parameters:

- **new\_frame\_number** ( _FrameNumber_) – What frame should this key be moved to? This should be in the time unit specified by TimeUnit.

- **sub\_frame** ( _float_) – If using Display Rate time, what is the sub-frame this should go to? Clamped [0-1), and ignored with when TimeUnit is set to Tick Resolution.\
\
- **time\_unit** ( _MovieSceneTimeUnit_) – Should the NewFrameNumber be interpreted as Display Rate frames or in Tick Resolution?\
\
\

---

**set_value**( _new_value_) → `None\`
\
Sets the value for this key, reflecting it in the owning channel.\
\
Parameters:\
\
**new\_value** ( _str_) – The new value for this key.\
\
### Table of Contents\
\
- `unreal.MovieSceneScriptingStringKey`\
  - `MovieSceneScriptingStringKey`\
    - `MovieSceneScriptingStringKey.get_time()`\
    - `MovieSceneScriptingStringKey.get_value()`\
    - `MovieSceneScriptingStringKey.set_time()`\
    - `MovieSceneScriptingStringKey.set_value()`\
\
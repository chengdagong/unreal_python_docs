# unreal.MovieSceneScriptingByteChannel

```python
class unreal.MovieSceneScriptingByteChannel(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MovieSceneScriptingChannel``


Movie Scene Scripting Byte Channel

**C++ Source:**

- **Plugin**: SequencerScripting

- **Module**: SequencerScripting

- **File**: MovieSceneScriptingByte.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `channel_name` (Name): [Read-Write]



---

**add_key**( _time_, _new_value_, _sub_frame=0.000000_, _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_, _interpolation=MovieSceneKeyInterpolation.AUTO_) → `MovieSceneScriptingByteKey`

Add a key to this channel. This initializes a new key and returns a reference to it.

Parameters:

- **time** ( _FrameNumber_) – The frame this key should go on. Respects TimeUnit to determine if it is a display rate frame or a tick resolution frame.

- **new\_value** ( _uint8_) – The value that this key should be created with.

- **sub\_frame** ( _float_) – Optional [0-1) clamped sub-frame to put this key on. Ignored if TimeUnit is set to Tick Resolution.\
\
- **time\_unit** ( _MovieSceneTimeUnit_) – Is the specified InTime in Display Rate frames or Tick Resolution.\
\
- **interpolation** ( _MovieSceneKeyInterpolation_) – Interpolation method the key should use.\
\
\
Returns:\
\
The key that was created with the specified values at the specified time.\
\
Return type:\
\
MovieSceneScriptingByteKey\
\

---

**get_default**() → `uint8\`
\
Get this channel’s default value that will be used when no keys are present. Only a valid\
value when HasDefault() returns true.\
\
Return type:\
\
uint8\
\

---

**get_keys**() → `Array\ [MovieSceneScriptingKey]\`
\
Gets all of the keys in this channel.\
\
Returns:\
\
An array of UMovieSceneScriptingByteKey’s contained by this channel. Returns all keys even if clipped by the owning section’s boundaries or outside of the current sequence play range.\
\
Return type:\
\
Array\ [MovieSceneScriptingKey]\
\

---

**get_keys_by_index**( _indices_) → `Array\ [MovieSceneScriptingKey]\`
\
Gets the keys in this channel specified by the specific index\
Indices: The indices from which to get the keys from\
\
Parameters:\
\
**indices** ( _Array_ _[_ _int32_ _]_)\
\
Returns:\
\
An array of UMovieSceneScriptingKey’s contained by this channel. Returns all keys specified by the indices, even if out of range.\
\
Return type:\
\
Array\ [MovieSceneScriptingKey]\
\

---

**has_default**() → `boolReturns:\`
\
Does this channel have a default value set?\
\
Return type:\
\
bool\
\

---

**remove_default**() → `None\`
\
Remove this channel’s default value causing the channel to have no effect where no keys are present\
\

---

**remove_key**( _key_) → `None\`
\
Removes the specified key. Does nothing if the key is not specified or the key belongs to another channel.\
\
Parameters:\
\
**key** ( _MovieSceneScriptingKey_)\
\

---

**set_default**( _default_value_) → `None\`
\
Set this channel’s default value that should be used when no keys are present.\
Sets bHasDefaultValue to true automatically.\
\
Parameters:\
\
**default\_value** ( _uint8_)\
\

---

**transform**( _offset_frame_, _scale_, _pivot_frame_, _scripting_range_, _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_) → `None\`
\
Transform the keys in time in the channel by an offset, scale and pivot\
\
Parameters:\
\
- **offset\_frame** ( _FrameNumber_) – The amount to offset the keys by\
\
- **scale** ( _double_) – The amount to scale the keys by\
\
- **pivot\_frame** ( _FrameNumber_) – The frame to pivot around when scaling the keys\
\
- **scripting\_range** ( _SequencerScriptingRange_) – The time range of the keys to transform\
\
- **time\_unit** ( _MovieSceneTimeUnit_) – Is the specified OffsetFrame, PivotFrame, and ScriptingRange in Display Rate frames or Tick Resolution.\
\
\
### Table of Contents\
\
- `unreal.MovieSceneScriptingByteChannel`\
  - `MovieSceneScriptingByteChannel`\
    - `MovieSceneScriptingByteChannel.add_key()`\
    - `MovieSceneScriptingByteChannel.get_default()`\
    - `MovieSceneScriptingByteChannel.get_keys()`\
    - `MovieSceneScriptingByteChannel.get_keys_by_index()`\
    - `MovieSceneScriptingByteChannel.has_default()`\
    - `MovieSceneScriptingByteChannel.remove_default()`\
    - `MovieSceneScriptingByteChannel.remove_key()`\
    - `MovieSceneScriptingByteChannel.set_default()`\
    - `MovieSceneScriptingByteChannel.transform()`\
\
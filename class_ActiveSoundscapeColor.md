# unreal.ActiveSoundscapeColor

```python
class unreal.ActiveSoundscapeColor(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Active Soundscape Color

**C++ Source:**

- **Plugin**: Soundscape

- **Module**: Soundscape

- **File**: SoundscapeColor.h



---

**is_playing**() → `bool`

Is playing

Return type:

bool


---

**play**( _color_volume=1.000000_, _color_pitch=1.000000_, _color_fade_in_time=1.000000_) → `None`

Play Active Soundscape Color

Parameters:

- **color\_volume** ( _float_)

- **color\_pitch** ( _float_)

- **color\_fade\_in\_time** ( _float_)



---

**stop**( _color_fade_out_time=1.000000_) → `None`

Stop Active Soundscape Color

Parameters:

**color\_fade\_out\_time** ( _float_)

### Table of Contents

- `unreal.ActiveSoundscapeColor`
  - `ActiveSoundscapeColor`
    - `ActiveSoundscapeColor.is_playing()`
    - `ActiveSoundscapeColor.play()`
    - `ActiveSoundscapeColor.stop()`
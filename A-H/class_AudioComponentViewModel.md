# unreal.AudioComponentViewModel

```python
class unreal.AudioComponentViewModel(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MVVMViewModelBase``


Viewmodel for binding audio component state to widgets.

**C++ Source:**

- **Plugin**: TechAudioTools

- **Module**: TechAudioTools

- **File**: AudioComponentViewModel.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `is_fading_in` (bool): [Read-Write] True if the audio component is fading in.

- `is_fading_out` (bool): [Read-Write] True if the audio component is fading out.

- `is_playing` (bool): [Read-Write] True if the audio component is playing.

- `is_stopped` (bool): [Read-Write] True if the audio component is stopped.

- `is_virtualized` (bool): [Read-Write] True if the audio component is virtualized.

- `play_state` (AudioComponentPlayState): [Read-Write] Returns the enumerated play state of the audio component.



---

_property_ `is_fading_in`: bool

[Read-Only] True if the audio component is fading in.

**Type:**

( bool)


---

_property_ `is_fading_out`: bool

[Read-Only] True if the audio component is fading out.

**Type:**

( bool)


---

_property_ `is_playing`: bool

[Read-Only] True if the audio component is playing.

**Type:**

( bool)


---

_property_ `is_stopped`: bool

[Read-Only] True if the audio component is stopped.

**Type:**

( bool)


---

_property_ `is_virtualized`: bool

[Read-Only] True if the audio component is virtualized.

**Type:**

( bool)


---

_property_ `play_state`: AudioComponentPlayState

[Read-Only] Returns the enumerated play state of the audio component.

**Type:**

( AudioComponentPlayState)


---

**set_audio_component**( _audio_component_) → `None`

Sets the audio component this viewmodel should bind to.

Parameters:

**audio\_component** ( _AudioComponent_)

### Table of Contents

- `unreal.AudioComponentViewModel`
  - `AudioComponentViewModel`
    - `AudioComponentViewModel.is_fading_in`
    - `AudioComponentViewModel.is_fading_out`
    - `AudioComponentViewModel.is_playing`
    - `AudioComponentViewModel.is_stopped`
    - `AudioComponentViewModel.is_virtualized`
    - `AudioComponentViewModel.play_state`
    - `AudioComponentViewModel.set_audio_component()`
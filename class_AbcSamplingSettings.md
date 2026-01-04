# unreal.AbcSamplingSettings

```python
class unreal.AbcSamplingSettings(sampling_type:AlembicSamplingType=Ellipsis, frame_steps:int=0, time_steps:float=0.0, frame_start:int=0, frame_end:int=0, skip_empty:bool=False)
```


**Bases:** ``StructBase``


Abc Sampling Settings

**C++ Source:**

- **Plugin**: AlembicImporter

- **Module**: AlembicLibrary

- **File**: AbcImportSettings.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `frame_end` (int32): [Read-Write] Ending index to stop sampling the animation at

- `frame_start` (int32): [Read-Write] Starting index to start sampling the animation from

- `frame_steps` (int32): [Read-Write] Steps to take when sampling the animation

- `sampling_type` (AlembicSamplingType): [Read-Write] Type of sampling performed while importing the animation

- `skip_empty` (bool): [Read-Write] Skip empty (pre-roll) frames and start importing at the frame which actually contains data

- `time_steps` (float): [Read-Write] Time steps to take when sampling the animation



---

_property_ `frame_end`: int

[Read-Write] Ending index to stop sampling the animation at

**Type:**

(int32)


---

_property_ `frame_start`: int

[Read-Write] Starting index to start sampling the animation from

**Type:**

(int32)


---

_property_ `frame_steps`: int

[Read-Write] Steps to take when sampling the animation

**Type:**

(int32)


---

_property_ `sampling_type`: AlembicSamplingType

[Read-Write] Type of sampling performed while importing the animation

**Type:**

( AlembicSamplingType)


---

_property_ `skip_empty`: bool

[Read-Write] Skip empty (pre-roll) frames and start importing at the frame which actually contains data

**Type:**

( bool)


---

_property_ `time_steps`: float

[Read-Write] Time steps to take when sampling the animation

**Type:**

( float)

### Table of Contents

- `unreal.AbcSamplingSettings`
  - `AbcSamplingSettings`
    - `AbcSamplingSettings.frame_end`
    - `AbcSamplingSettings.frame_start`
    - `AbcSamplingSettings.frame_steps`
    - `AbcSamplingSettings.sampling_type`
    - `AbcSamplingSettings.skip_empty`
    - `AbcSamplingSettings.time_steps`
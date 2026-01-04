# unreal.AnimNotify_GameplayCue

```python
class unreal.AnimNotify_GameplayCue(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``AnimNotify``


UAnimNotify\_GameplayCue

> An animation notify used for instantaneous gameplay cues (Burst/Latent).

**C++ Source:**

- **Plugin**: GameplayAbilities

- **Module**: GameplayAbilities

- **File**: AnimNotify\_GameplayCue.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `gameplay_cue` (GameplayCueTag): [Read-Write] GameplayCue tag to invoke.

- `notify_color` (Color): [Read-Write] Color of Notify in editor

- `should_fire_in_editor` (bool): [Read-Write] Whether this notify instance should fire in animation editors



---

_property_ `gameplay_cue`: GameplayCueTag

[Read-Only] GameplayCue tag to invoke.

**Type:**

( GameplayCueTag)

### Table of Contents

- `unreal.AnimNotify_GameplayCue`
  - `AnimNotify_GameplayCue`
    - `AnimNotify_GameplayCue.gameplay_cue`
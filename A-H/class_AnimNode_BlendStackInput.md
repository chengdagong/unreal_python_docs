# unreal.AnimNode_BlendStackInput

```python
class unreal.AnimNode_BlendStackInput
```


**Bases:** ``AnimNode_Base``


Input pose that links the blend stack’s sample graph with the sample/pose chosen by the blend stack.
Todo:: It might be better to reuse FAnimNode\_LinkedInputPose, since we will most likely need variable input pins in the future too.

**C++ Source:**

- **Plugin**: BlendStack

- **Module**: BlendStack

- **File**: AnimNode\_BlendStackInput.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `override_play_rate` (bool): [Read-Write] If true, the PlayRate input from thos node will override the SequencePlayer or BlendSpacePlayer playrate each frame

- `play_rate` (float): [Read-Write] The play rate multiplier. Can be negative, which will cause the animation to play in reverse.


### Table of Contents

- `unreal.AnimNode_BlendStackInput`
  - `AnimNode_BlendStackInput`
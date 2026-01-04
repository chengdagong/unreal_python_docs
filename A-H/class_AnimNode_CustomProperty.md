# unreal.AnimNode_CustomProperty

```python
class unreal.AnimNode_CustomProperty
```


**Bases:** ``AnimNode_Base``


Custom property node that you’d like to expand pin by reflecting internal instance (we call TargetInstance here)

> Used by sub anim instance or control rig node
>
> where you have internal instance and would like to reflect to AnimNode as a pin
>
> To make pin working, you need storage inside of AnimInstance (SourceProperties/SourcePropertyNames)
> So this creates storage inside of AnimInstance with the unique custom property name
>
> > and it copies to the actually TargetInstance here to allow the information be transferred in runtime (DestProperties/DestPropertyNames)
>
> TargetInstance - UObject derived instance that has certain dest properties
> Source - AnimInstance’s copy properties that is used to store the data

**C++ Source:**

- **Module**: Engine

- **File**: AnimNode\_CustomProperty.h


### Table of Contents

- `unreal.AnimNode_CustomProperty`
  - `AnimNode_CustomProperty`
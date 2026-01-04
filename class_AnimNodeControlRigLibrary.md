# unreal.AnimNodeControlRigLibrary

```python
class unreal.AnimNodeControlRigLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Exposes operations to be performed on a control rig anim node

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: AnimNode\_ControlRig\_Library.h


_classmethod_ convert\_to\_control\_rig( _node)->(ControlRigReference_, _result=AnimNodeReferenceConversionResult_)

Get a control rig context from an anim node context

Parameters:

**node** ( _AnimNodeReference_)

Returns:

result (AnimNodeReferenceConversionResult):

Return type:

AnimNodeReferenceConversionResult

_classmethod_ convert\_to\_control\_rig\_pure( _node)->(control\_rig=ControlRigReference_, _result=bool_)

Get a control rig context from an anim node context (pure)

Parameters:

**node** ( _AnimNodeReference_)

Returns:

control\_rig (ControlRigReference):

result (bool):

Return type:

tuple


---

_classmethod_ set_control_rig_class( _node_, _control_rig_class_)→ControlRigReference

Set the control rig class on the node

Parameters:

- **node** ( _ControlRigReference_)

- **control\_rig\_class** ( _type_ _(_ _Class_ _)_)


Return type:

ControlRigReference

### Table of Contents

- `unreal.AnimNodeControlRigLibrary`
  - `AnimNodeControlRigLibrary`
    - `AnimNodeControlRigLibrary.convert_to_control_rig()`
    - `AnimNodeControlRigLibrary.convert_to_control_rig_pure()`
    - `AnimNodeControlRigLibrary.set_control_rig_class()`
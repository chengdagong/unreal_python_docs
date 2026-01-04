# unreal.RemoteControlInterceptionTestObject

```python
class unreal.RemoteControlInterceptionTestObject(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Remote Control Interception Test Object

**C++ Source:**

- **Plugin**: RemoteControl

- **Module**: RemoteControl

- **File**: RemoteControlInterceptionTestData.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `custom_struct` (RemoteControlInterceptionTestStruct): [Read-Write]

- `function_param_struct` (RemoteControlInterceptionFunctionParamStruct): [Read-Write]

- `value_with_setter` (str): [Read-Write] Testing private property with a setter.



---

**test_function**( _struct_, _test_factor_) → `RemoteControlInterceptionFunctionParamStruct`

Test Function

Parameters:

- **struct** ( _RemoteControlInterceptionFunctionParamStruct_)

- **test\_factor** ( _int32_)


Return type:

RemoteControlInterceptionFunctionParamStruct

### Table of Contents

- `unreal.RemoteControlInterceptionTestObject`
  - `RemoteControlInterceptionTestObject`
    - `RemoteControlInterceptionTestObject.test_function()`
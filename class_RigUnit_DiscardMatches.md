# unreal.RigUnit_DiscardMatches

```python
class unreal.RigUnit_DiscardMatches(execute_pin:RigVMExecutePin=\[\], excluded:None=\[\], message:str='')
```


**Bases:** ``RigUnitMutable``


Discards matches during a connector event

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_ConnectionCandidates.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `excluded` (Array[RigElementKey]): [Read-Write] The items being interacted on

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `message` (str): [Read-Write]



---

_property_ `excluded`: None

[Read-Write] The items being interacted on

**Type:**

( Array\ [RigElementKey])


---

_property_ `message`: str

[Read-Write]

**Type:**

( str)

### Table of Contents

- `unreal.RigUnit_DiscardMatches`
  - `RigUnit_DiscardMatches`
    - `RigUnit_DiscardMatches.excluded`
    - `RigUnit_DiscardMatches.message`
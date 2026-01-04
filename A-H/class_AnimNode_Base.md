# unreal.AnimNode_Base

```python
class unreal.AnimNode_Base
```


**Bases:** ``StructBase``


This is the base of all runtime animation nodes

To create a new animation node:

Create a struct derived from FAnimNode\_Base - this is your runtime node
Create a class derived from UAnimGraphNode\_Base, containing an instance of your runtime node as a member - this is your visual/editor-only node

**C++ Source:**

- **Module**: Engine

- **File**: AnimNodeBase.h


### Table of Contents

- `unreal.AnimNode_Base`
  - `AnimNode_Base`
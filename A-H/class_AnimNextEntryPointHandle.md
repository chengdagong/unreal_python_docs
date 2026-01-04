# unreal.AnimNextEntryPointHandle

```python
class unreal.AnimNextEntryPointHandle
```


**Bases:** ``StructBase``


Entry Point Handle
An entry point handle is equivalent to a trait handle but it will not resolve automatically on load.
As such, it is safe to use outside of an AnimNext graph.
They must be manually resolved through FTraitReader.

Internally, it contains a node handle (as a node ID) and a trait index.
see: FAnimNextTraitHandle, FTraitReader

**C++ Source:**

- **Plugin**: UAFAnimGraph

- **Module**: UAFAnimGraph

- **File**: EntryPointHandle.h


### Table of Contents

- `unreal.AnimNextEntryPointHandle`
  - `AnimNextEntryPointHandle`
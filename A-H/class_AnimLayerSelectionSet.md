# unreal.AnimLayerSelectionSet

```python
class unreal.AnimLayerSelectionSet(bound_object:Object=Ellipsis, names:None={})
```


**Bases:** ``StructBase``


Bound object/control rig and the properties/channels it is made of
A layer will consist of a bunch of these

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRigEditor

- **File**: AnimLayers.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bound_object` (Object): [Read-Write]

- `names` (Map[Name, AnimLayerPropertyAndChannels]): [Read-Write] bound object is either a CR or a bound sequencer object



---

_property_ `bound_object`: Object

[Read-Write]

**Type:**

( Object)


---

_property_ `names`: None

[Read-Write] bound object is either a CR or a bound sequencer object

**Type:**

( Map\ [Name, AnimLayerPropertyAndChannels])

### Table of Contents

- `unreal.AnimLayerSelectionSet`
  - `AnimLayerSelectionSet`
    - `AnimLayerSelectionSet.bound_object`
    - `AnimLayerSelectionSet.names`
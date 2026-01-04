# unreal.NiagaraDataInterfaceUObjectPropertyReader

```python
class unreal.NiagaraDataInterfaceUObjectPropertyReader(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``NiagaraDataInterface``


Data interface to read properties from UObjects.
Rather than having BP tick functions that push data into Niagara this data interface will instead pull them.

**C++ Source:**

- **Plugin**: Niagara

- **Module**: Niagara

- **File**: NiagaraDataInterfaceUObjectPropertyReader.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `property_remap` (Array[NiagaraUObjectPropertyReaderRemap]): [Read-Write]

- `source_actor` (Actor): [Read-Write] Optional source actor to use, if the user parameter binding is valid this will be ignored.

- `source_actor_component_class` (type(Class)): [Read-Write] When an actor is bound as the object we will also search for a component of this type to bind properties to.
For example, setting this to a UPointLightComponent when binding properties we will first look at the actor
then look for a component of UPointLightComponent and look at properties on that also.
If no class is specified here we look at the RootComponent instead.

- `source_mode` (NDIObjectPropertyReaderSourceMode): [Read-Write] Determines how we should select the source object we read from.

- `u_object_parameter_binding` (NiagaraUserParameterBinding): [Read-Write] User parameter Object binding to read properties from.



---

_classmethod_ set_u_object_reader_property_remap( _niagara_component_, _user_parameter_name_, _graph_name_, _remap_name_)→None

Remaps a property reader, where the

Parameters:

- **niagara\_component** ( _NiagaraComponent_)

- **user\_parameter\_name** ( _Name_)

- **graph\_name** ( _Name_)

- **remap\_name** ( _Name_)


### Table of Contents

- `unreal.NiagaraDataInterfaceUObjectPropertyReader`
  - `NiagaraDataInterfaceUObjectPropertyReader`
    - `NiagaraDataInterfaceUObjectPropertyReader.set_u_object_reader_property_remap()`
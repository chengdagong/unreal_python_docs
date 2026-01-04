# unreal.StructBase

```python
class unreal.StructBase(\*args:Any, \*\*kwargs:Any)
```


**Bases:** ``_WrapperBase``


Type for all Unreal exposed struct instances


---

**__copy__**( _self_)→Any--copythisUnrealstructassign(_self_, _other:object_)→None--assignthevalueofthisUnrealstructtovalueofthegivenobject_classmethod_ cast(_cls:Type[_T]_, _object:object |Mapping\ [str, object]|Iterable\ [object]_)→_T--castthegivenobjecttothisUnrealstructtype.CanbepartialMapping[fieldName, fiedValue]orasequenceoffieldvaluescopy(_self_)→Any--copythisUnrealstructexport_text(_self_)→str--exportsthecontentoftheUnrealstructofthistypeget_editor_property(_self_, _name:Name | str_)→object--getthevalueofanypropertyvisibletotheeditorimport_text(_self_, _content:str_)→bool--importstheprovidedstringintotheUnrealstructset_editor_properties(_self_, _properties:Mapping\ [str, object]_)→None--setthevalueofanypropertiesvisibletotheeditor(fromaname->valuedict), ensuringthatthepre/postchangenotificationsarecalledset_editor_property(_self_, _name:Name | str_, _value:object_, _notify_mode:PropertyAccessChangeNotifyMode=PropertyAccessChangeNotifyMode.DEFAULT_)→None--setthevalueofanypropertyvisibletotheeditor, ensuringthatthepre/postchangenotificationsarecalled_classmethod_ static_struct(_cls_)→ScriptStruct--gettheUnrealstructofthistypeto_tuple(_self_) → `Tuple[object,...]--breakthisUnrealstructintoatupleofitsproperties`

### Table of Contents

- `unreal.StructBase`
  - `StructBase`
    - `StructBase.__copy__()`
    - `StructBase.assign()`
    - `StructBase.cast()`
    - `StructBase.copy()`
    - `StructBase.export_text()`
    - `StructBase.get_editor_property()`
    - `StructBase.import_text()`
    - `StructBase.set_editor_properties()`
    - `StructBase.set_editor_property()`
    - `StructBase.static_struct()`
    - `StructBase.to_tuple()`
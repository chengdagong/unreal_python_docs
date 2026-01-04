# unreal._ObjectBase

```python
class unreal.ObjectBase(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``_WrapperBase``


Type for all Unreal exposed object instances


---

**call_method**( _self_, _name:str_, _\*args:Tuple\ [object, ...]_, _\*\*kwargs:Mapping\ [str, object]_)→Any--callamethodonthisobjectviaUnrealreflectionusingthegivenordered(atuplepassedasargs)ornamed(adictpassedaskwargs)argumentdata-allowscallingmethodsthatdon'thavePythonglue_classmethod_ cast(_cls:Type[_T]_, _object:object_)→_T--castthegivenobjecttothisUnrealobjecttypeorraiseanexceptionifthecastisnotpossibleget_class(_self_)→Class--gettheUnrealclassofthisinstance_classmethod_ get_default_object(_cls:Type[_T]_)→_T--gettheUnrealclassdefaultobject(CDO)ofthistypeget_editor_property(_self_, _name:str_)→object--getthevalueofanypropertyvisibletotheeditorget_fname(_self_)→Name--getthenameofthisinstanceget_full_name(_self_)→str--getthefullname(classname+fullpath)ofthisinstanceget_name(_self_)→str--getthenameofthisinstanceget_outer(_self)->Any--gettheouterobjectfromthisinstance(ifany_)get_outermost(_self_)→Package--gettheoutermostobject(thepackage)fromthisinstanceget_package(_self_)→Package--getthepackagedirectlyassociatedwiththisinstanceget_path_name(_self_)→str--getthepathnameofthisinstanceget_typed_outer(_self_, _type:Union[Class_, _type])->Any--getthefirstouterobjectofthegiventypefromthisinstance(ifany_)get_world(_self)->Optional[World]--gettheworldassociatedwiththisinstance(ifany_)is_package_external(_self_)→bool--returnstrueifthisinstancehasadifferentpackagethanitsouter'spackagemodify(_self_, _always_mark_dirty:bool=True)->bool--informthatthisinstanceisabouttobemodified(trackschangesforundo/redoiftransactional_)rename(_self_, _name:Name | str='None'_, _outer:Object | None=None_)→bool--renamethisinstanceand/orchangeitsouterset_editor_properties(_self_, _properties:Mapping\ [str, object]_)→None--setthevalueofanypropertiesvisibletotheeditor(fromaname->valuedict), ensuringthatthepre/postchangenotificationsarecalledset_editor_property(_self_, _name:str_, _value:object_, _notify_mode:PropertyAccessChangeNotifyMode=PropertyAccessChangeNotifyMode.DEFAULT_)→None--setthevalueofanypropertyvisibletotheeditor, ensuringthatthepre/postchangenotificationsarecalled_classmethod_ static_class(_cls_) → `Class--gettheUnrealclassofthistype`

### Table of Contents

- `unreal._ObjectBase`
  - `_ObjectBase`
    - `_ObjectBase.call_method()`
    - `_ObjectBase.cast()`
    - `_ObjectBase.get_class()`
    - `_ObjectBase.get_default_object()`
    - `_ObjectBase.get_editor_property()`
    - `_ObjectBase.get_fname()`
    - `_ObjectBase.get_full_name()`
    - `_ObjectBase.get_name()`
    - `_ObjectBase.get_outer()`
    - `_ObjectBase.get_outermost()`
    - `_ObjectBase.get_package()`
    - `_ObjectBase.get_path_name()`
    - `_ObjectBase.get_typed_outer()`
    - `_ObjectBase.get_world()`
    - `_ObjectBase.is_package_external()`
    - `_ObjectBase.modify()`
    - `_ObjectBase.rename()`
    - `_ObjectBase.set_editor_properties()`
    - `_ObjectBase.set_editor_property()`
    - `_ObjectBase.static_class()`
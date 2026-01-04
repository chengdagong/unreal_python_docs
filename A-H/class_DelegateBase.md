# unreal.DelegateBase

```python
class unreal.DelegateBase(\*args:Any, \*\*kwargs:Any)
```


**Bases:** ``_WrapperBase``


Type for all Unreal exposed delegate instances


---

**__copy__**( _self_)→Any--copythisUnrealdelegatebind_callable(_self_, _callable:Callable[..., Any]_)→None--bindthisUnrealdelegatetoaPythoncallablebind_delegate(_self_, _delegate:DelegateBase_)→None--bindthisUnrealdelegatetothesameobjectandfunctionasanotherdelegatebind_function(_self_, _obj:Object_, _name:Name | str_)→None--bindthisUnrealdelegatetoanamedUnrealfunctiononthegivenobjectinstance_classmethod_ cast(_cls:Type[_T]_, _object:object_)→_T--castthegivenobjecttothisUnrealdelegatetypecopy(_self_)→Any--copythisUnrealdelegateexecute(_self_, _\*args:Any_)→Any--callthisUnrealdelegate, buterrorifit'sunboundexecute_if_bound(_self_, _\*args:Any_)→Any--callthisUnrealdelegate, butonlyifit'sboundtosomethingis_bound(_self_)→bool--isthisUnrealdelegateboundtosomething?unbind(_self_) → `None--unbindthisUnrealdelegate`

### Table of Contents

- `unreal.DelegateBase`
  - `DelegateBase`
    - `DelegateBase.__copy__()`
    - `DelegateBase.bind_callable()`
    - `DelegateBase.bind_delegate()`
    - `DelegateBase.bind_function()`
    - `DelegateBase.cast()`
    - `DelegateBase.copy()`
    - `DelegateBase.execute()`
    - `DelegateBase.execute_if_bound()`
    - `DelegateBase.is_bound()`
    - `DelegateBase.unbind()`
# unreal.MulticastDelegateBase

```python
class unreal.MulticastDelegateBase(\*args:Any, \*\*kwargs:Any)
```


**Bases:** ``_WrapperBase``


Type for all Unreal exposed multicast delegate instances


---

**__copy__**( _self_)→Any--copythisUnrealdelegateadd_callable(_self_, _callable:Callable[..., Any]_)→None--addabindingtoaPythoncallabletotheinvocationlistofthisUnrealdelegateadd_callable_unique(_self_, _callable:Callable[..., Any]_)→None--addauniquebindingtoaPythoncallabletotheinvocationlistofthisUnrealdelegateadd_function(_self_, _obj:Object_, _name:Name | str_)→None--addabindingtoanamedUnrealfunctiononthegivenobjectinstancetotheinvocationlistofthisUnrealdelegateadd_function_unique(_self_, _obj:Object_, _name:Name | str_)→None--addauniquebindingtoanamedUnrealfunctiononthegivenobjectinstancetotheinvocationlistofthisUnrealdelegatebroadcast(_\*args:Any_)→None--invokethisUnrealmulticastdelegate_classmethod_ cast(_cls:Type[_T]_, _object:object_)→_T--castthegivenobjecttothisUnrealdelegatetypeclear()→None--cleartheinvocationlistofthisUnrealdelegatecontains_callable(_self_, _callable:Callable[..., Any]_)→bool--doestheinvocationlistofthisUnrealdelegatecontainabindingtoaPythoncallablecontains_function(_self_, _obj:Object_, _name:Name | str_)→bool--doestheinvocationlistofthisUnrealdelegatecontainabindingtoanamedUnrealfunctiononthegivenobjectinstancecopy(_self_)→Any--copythisUnrealdelegateis_bound(_self_)→bool--isthisUnrealdelegateboundtosomething?remove_callable(_self_, _callable:Callable[..., Any]_)→None--removeabindingtoaPythoncallablefromtheinvocationlistofthisUnrealdelegateremove_function(_self_, _obj:Object_, _name:Name | str_)→None--removeabindingtoanamedUnrealfunctiononthegivenobjectinstancefromtheinvocationlistofthisUnrealdelegateremove_object(_self_, _obj:Object_) → `None--removeallbindingsforthegivenobjectinstancefromtheinvocationlistofthisUnrealdelegate`

### Table of Contents

- `unreal.MulticastDelegateBase`
  - `MulticastDelegateBase`
    - `MulticastDelegateBase.__copy__()`
    - `MulticastDelegateBase.add_callable()`
    - `MulticastDelegateBase.add_callable_unique()`
    - `MulticastDelegateBase.add_function()`
    - `MulticastDelegateBase.add_function_unique()`
    - `MulticastDelegateBase.broadcast()`
    - `MulticastDelegateBase.cast()`
    - `MulticastDelegateBase.clear()`
    - `MulticastDelegateBase.contains_callable()`
    - `MulticastDelegateBase.contains_function()`
    - `MulticastDelegateBase.copy()`
    - `MulticastDelegateBase.is_bound()`
    - `MulticastDelegateBase.remove_callable()`
    - `MulticastDelegateBase.remove_function()`
    - `MulticastDelegateBase.remove_object()`
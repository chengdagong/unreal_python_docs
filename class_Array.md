# unreal.Array

```python
class unreal.Array(type:type)
```


**Bases:** ``_WrapperBase`, `MutableSequence`[`_ElemType`]`


Type for all Unreal exposed array instances

_classmethod_\_\_class\_getitem\_\_( _\*args_)

\_\_class\_getitem\_\_(cls, item: \_ElemType) – implemented for type hinting purpose only


---

**__copy__**( _self_)→Array[_ElemType]--copythisUnrealarrayappend(_self_, _value:_ElemType)->None--appendthegivenvaluetotheendofthisUnrealarray(equivalenttoTArray::AddinC++_)_classmethod_ cast(_cls_, _type:Type[_ElemType]_, _obj:object_)→Array[_ElemType]--castthegivenobjecttothisUnrealarraytypeclear(_self_)→None--removeallvaluesfromthisUnrealarraycopy(_self_)→Array[_ElemType]--copythisUnrealarraycount(_self_, _value:_ElemType_)→int--returnthenumberoftimesthatvalueappearsinthisthisUnrealarrayextend(_self_, _values:Iterable[_ElemType])->None--extendthisUnrealarraybyappendingelementsfromthegiveniterable(equivalenttoTArray::AppendinC++_)index(_self_, _value:_ElemType_, _start:int=0_, _stop:int=-1)->int--gettheindexofthefirstmatchingvalueinthisUnrealarray_, _orraiseValueErrorifmissing(equivalenttoTArray::IndexOfByKeyinC++_)insert(_self_, _index:int_, _value:_ElemType_)→None--insertthegivenvalueatthegivenindexinthisUnrealarraypop(_self_, _index:int=-1_)→_ElemType--removeandreturnthevalueatthegivenindexinthisUnrealarray, orraiseIndexErroriftheindexisout-of-boundsremove(_self_, _value:_ElemType_)→None--removethefirstmatchingvalueinthisUnrealarray, orraiseValueErrorifmissingresize(_self_, _len:int_)→None--resizethisUnrealarraytoholdthegivennumberofelementsreverse(_self_)→None--reversethisUnrealarrayin-placesort(_self_, _key:Callable[[_ElemType], object]| None=None_, _reverse:bool=False_) → `None--stablesortthisUnrealarrayin-place`

### Table of Contents

- `unreal.Array`
  - `Array`
    - `Array.__class_getitem__()`
    - `Array.__copy__()`
    - `Array.append()`
    - `Array.cast()`
    - `Array.clear()`
    - `Array.copy()`
    - `Array.count()`
    - `Array.extend()`
    - `Array.index()`
    - `Array.insert()`
    - `Array.pop()`
    - `Array.remove()`
    - `Array.resize()`
    - `Array.reverse()`
    - `Array.sort()`
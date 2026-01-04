# unreal.Set

```python
class unreal.Set(type:type)
```


**Bases:** ``_WrapperBase`, `MutableSet`[`_ElemType`]`


Type for all Unreal exposed set instances

_classmethod_\_\_class\_getitem\_\_( _\*args_)

\_\_class\_getitem\_\_(cls, item: \_ElemType) – implemented for type hinting purpose only


---

**__copy__**( _self_)→Set[_ElemType]--copythisUnrealsetadd(_self_, _value:_ElemType_)→None--addthegivenvaluetothisUnrealsetifnotalreadypresent_classmethod_ cast(_cls_, _type:Type[_ElemType]_, _obj:object_)→Set[_ElemType]--castthegivenobjecttothisUnrealsettypeclear(_self_)→None--removeallvaluesfromthisUnrealsetcopy(_self_)→Set[_ElemType]--copythisUnrealsetdifference(_self_, _\*iterable:Iterable[_ElemType])->Set[_ElemType]--returnthedifferencebetweenthisUnrealsetandtheotheriterablespassedforcomparison(ie_, _allvaluesthatareinthissetbutnottheothers_)difference_update(_self_, _\*iterables:Iterable[_ElemType])->None--makethissetthedifferencebetweenthisUnrealsetandtheotheriterablespassedforcomparison(ie_, _allvaluesthatareinthissetbutnottheothers_)discard(_self_, _value:_ElemType_)→None--removethegivenvaluefromthisUnrealset, ordonothingifnotpresentintersection(_self_, _\*iterables:Iterable[_ElemType])->Set[_ElemType]--returntheintersectionbetweenthisUnrealsetandtheotheriterablespassedforcomparison(ie_, _valuesthatarecommontoallofthesets_)intersection_update(_self_, _\*iterables:Iterable[_ElemType])->None--makethissettheintersectionbetweenthisUnrealsetandtheotheriterablespassedforcomparison(ie_, _valuesthatarecommontoallofthesets_)isdisjoint(_self_, _other:Iterable[_ElemType]_)→bool--returnTrueifthereisanullintersectionbetweenthisUnrealsetandanotherissubset(_self_, _other:Iterable[_ElemType]_)→bool--returnTrueifanothersetcontainsthisUnrealsetissuperset(_self_, _other:Iterable[_ElemType]_)→bool--returnTrueifthisUnrealsetcontainsanotherpop(_self_)→_ElemType--removeandreturnanarbitraryvaluefromthisUnrealset, orraiseKeyErrorifthesetisemptyremove(_self_, _value:_ElemType_) → `None--removethegivenvaluefromthisUnrealset,orraiseKeyErrorifnotpresentsymmetric_difference( _self_, _other:Iterable[_ElemType])->Set[_ElemType]--returnthesymmetricdifferencebetweenthisUnrealsetandanother(ie_, _valuesthatareinexactlyoneofthesets_)symmetric_difference_update( _self_, _other:Iterable[_ElemType])->None--makethissetthesymmetricdifferencebetweenthisUnrealsetandanother(ie_, _valuesthatareinexactlyoneofthesets_)union( _self_, _\*iterables:Iterable[_ElemType])->Set[_ElemType]--returntheunionbetweenthisUnrealsetandtheotheriterablespassedforcomparison(ie_, _valuesthatareinanyset_)update( _self_, _\*iterables:Iterable[_ElemType])->None--makethissettheunionbetweenthisUnrealsetandtheotheriterablespassedforcomparison(ie_, _valuesthatareinanyset_)`

### Table of Contents

- `unreal.Set`
  - `Set`
    - `Set.__class_getitem__()`
    - `Set.__copy__()`
    - `Set.add()`
    - `Set.cast()`
    - `Set.clear()`
    - `Set.copy()`
    - `Set.difference()`
    - `Set.difference_update()`
    - `Set.discard()`
    - `Set.intersection()`
    - `Set.intersection_update()`
    - `Set.isdisjoint()`
    - `Set.issubset()`
    - `Set.issuperset()`
    - `Set.pop()`
    - `Set.remove()`
    - `Set.symmetric_difference()`
    - `Set.symmetric_difference_update()`
    - `Set.union()`
    - `Set.update()`
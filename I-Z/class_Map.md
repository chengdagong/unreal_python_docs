# unreal.Map

```python
class unreal.Map(key:type, value:type)
```


**Bases:** ``_WrapperBase`, `MutableMapping`[`_KeyType`, `_ValueType`]`


Type for all Unreal exposed map instances

_classmethod_\_\_class\_getitem\_\_( _\*args_)

\_\_class\_getitem\_\_(cls, item) – implemented for type hinting purpose only


---

**__copy__**( _self_)→Map[_KeyType, _ValueType]--copythisUnrealmap_classmethod_ cast(_cls_, _key:Type[_KeyType]_, _value:Type[_ValueType]_, _obj:object_)→Map[_KeyType, _ValueType]--castthegivenobjecttothisUnrealmaptypeclear(_self_)→None--removeallitemsfromthisUnrealmapcopy(_self_)→Map[_KeyType, _ValueType]--copythisUnrealmap_classmethod_ fromkeys(_cls, sequence:Iterable[_KeyType], value:_ValueType)->Map[_KeyType, _ValueType]--returnsanewUnrealmapofkeysfromthesequenceusingthegivenvalue(typesareinferred_)get(_self_, _key:_KeyType_, _default:_ValueType=..._)→_ValueType--x[key]ifkeyinx, otherwisedefaultitems(_self_)→ItemsView[_KeyType, _ValueType]--aset-likeviewofthekey->valuepairsofthisUnrealmapkeys(_self_)→KeysView[_KeyType]--aset-likeviewofthekeysofthisUnrealmappop(_self_, _key:_KeyType_, _default:_ValueType=..._)→_ValueType--removekeyandreturnitsvalue, ordefaultifkeynotpresent, orraiseKeyErrorifnodefaultpopitem(_self_)→Tuple[_KeyType, _ValueType]--removeandreturnanarbitrarypairfromthisUnrealmap, orraiseKeyErrorifthemapisemptysetdefault(_self_, _key:_KeyType_, _default:_ValueType=..._)→_ValueType--setkeytodefaultifkeynotinxandreturnthevalueofkeyupdate(_self_, _pairs:Mapping[_KeyType, _ValueType]|Iterable[Tuple[_KeyType, _ValueType]]|Iterable[List[_KeyType|_ValueType]]_)→None--updatethisUnrealmapfromthegivenmappingorsequencepairstypeorkey->valueargumentsvalues(_self_) → `ValuesView[_ValueType]--aviewofthevaluesofthisUnrealmap`

### Table of Contents

- `unreal.Map`
  - `Map`
    - `Map.__class_getitem__()`
    - `Map.__copy__()`
    - `Map.cast()`
    - `Map.clear()`
    - `Map.copy()`
    - `Map.fromkeys()`
    - `Map.get()`
    - `Map.items()`
    - `Map.keys()`
    - `Map.pop()`
    - `Map.popitem()`
    - `Map.setdefault()`
    - `Map.update()`
    - `Map.values()`
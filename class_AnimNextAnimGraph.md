# unreal.AnimNextAnimGraph

```python
class unreal.AnimNextAnimGraph(asset:Object=Ellipsis, injection_data:AnimNextGraphInjectionData=\[\], host_graph:AnimNextAnimationGraph=Ellipsis)
```


**Bases:** ``StructBase``


Represents an instance of an AnimNext graph, either an asset or some externally-provided graph instance.
The asset can be set to refer directly to a graph asset, or it can be used via a ‘factory’ to generate an appropriate graph to run.
When public, represents an ‘injection site’ that can be used to parameterize graph execution externally.

**C++ Source:**

- **Plugin**: UAFAnimGraph

- **Module**: UAFAnimGraph

- **File**: AnimNextAnimGraph.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset` (Object): [Read-Write] The asset to run as an animation graph

- `host_graph` (AnimNextAnimationGraph): [Read-Write] The host graph to use to run the asset. Applies only to top-level graphs being run in modules.
We use a host graph to be able to blend between graph sources at the top level of a module when a RunGraph’s input graph changes.
If this is unset, then the project’s default host graph will be used.

- `injection_data` (AnimNextGraphInjectionData): [Read-Only] Injection data used to override the supplied graph



---

_property_ `asset`: Object

[Read-Write] The asset to run as an animation graph

**Type:**

( Object)


---

_property_ `host_graph`: AnimNextAnimationGraph

[Read-Write] The host graph to use to run the asset. Applies only to top-level graphs being run in modules.
We use a host graph to be able to blend between graph sources at the top level of a module when a RunGraph’s input graph changes.
If this is unset, then the project’s default host graph will be used.

**Type:**

( AnimNextAnimationGraph)


---

_property_ `injection_data`: AnimNextGraphInjectionData

[Read-Only] Injection data used to override the supplied graph

**Type:**

( AnimNextGraphInjectionData)

### Table of Contents

- `unreal.AnimNextAnimGraph`
  - `AnimNextAnimGraph`
    - `AnimNextAnimGraph.asset`
    - `AnimNextAnimGraph.host_graph`
    - `AnimNextAnimGraph.injection_data`
# unreal.UsdStageImportOptions

```python
class unreal.UsdStageImportOptions(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Usd Stage Import Options

**C++ Source:**

- **Plugin**: USDImporter

- **Module**: USDStageImporter

- **File**: USDStageImportOptions.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `existing_actor_policy` (ReplaceActorPolicy): [Read-Write] What should happen when imported actors and components try to overwrite existing actors and components

- `existing_asset_cache` (SoftObjectPath): [Read-Write] Copy assets from an existing UsdAsset cache instead of generating them from scratch, if possible

- `existing_asset_policy` (ReplaceAssetPolicy): [Read-Write] What should happen when imported assets try to overwrite existing assets

- `fallback_collision_type` (UsdCollisionType): [Read-Write] What type of collision to use for static meshes generated from Prims that don’t have physics schemas applied

- `groom_interpolation_settings` (Array[HairGroupsInterpolation]): [Read-Write] Groom group interpolation settings

- `import_actors` (bool): [Read-Write]

- `import_at_specific_time_code` (bool): [Read-Write] When true the stage will be evaluated at ImportTimeCode for the import.
When false, the stage will be evaluated at the default (non-animated) timecode

- `import_geometry` (bool): [Read-Write]

- `import_groom_assets` (bool): [Read-Write] Whether to import GroomAssets, GroomCaches and GroomBindings

- `import_level_sequences` (bool): [Read-Write]

- `import_materials` (bool): [Read-Write]

- `import_only_used_materials` (bool): [Read-Write] If this is checked, only materials actively used by the stage and import settings will be parsed.
If this is unchecked, all materials present on the stage will be parsed.

- `import_skeletal_animations` (bool): [Read-Write] Whether to try importing UAnimSequence skeletal animation assets for each encountered UsdSkelAnimQuery

- `import_sounds` (bool): [Read-Write] Whether to import audio files referenced by UsdMediaSpatialAudio schemas as Unreal sound assets

- `import_sparse_volume_textures` (bool): [Read-Write] Whether to import OpenVDB volumes as Sparse Volume Textures

- `import_time_code` (float): [Read-Write] TimeCode to evaluate the stage for import, in case bImportAtSpecificTimeCode is enabled

- `interpret_lods` (bool): [Read-Write] When true, if a prim has a “LOD” variant set with variants named “LOD0”, “LOD1”, etc. where each contains a UsdGeomMesh, the importer will
attempt to parse the meshes as separate LODs of a single UStaticMesh. When false, only the selected variant will be parsed as LOD0 of the
UStaticMesh.

- `kinds_to_collapse` (int32): [Read-Write] Whether to try to combine individual assets and components of the same type on a kind-per-kind basis,
like multiple Mesh prims into a single Static Mesh

- `material_purpose` (Name): [Read-Write] Specifies which material purpose to use when parsing USD material bindings, in addition to the “allPurpose” fallback

- `merge_identical_material_slots` (bool): [Read-Write] Identical material slots will be combined into a single slot if this is enabled. This is only performed in the context
of mesh collapsing, or when parsing LOD variant sets (see bInterpretLODs)

- `metadata_options` (UsdMetadataImportOptions): [Read-Write] Describes if/how we should collect metadata from USD prims onto the assets and components we generate when importing

- `nanite_triangle_threshold` (int32): [Read-Write] Try enabling Nanite for static meshes that are generated with at least this many triangles

- `override_stage_options` (bool): [Read-Write] Whether to use the specified StageOptions instead of the stage’s own settings

- `prim_path_folder_structure` (bool): [Read-Write] When enabled, assets will be imported into a content folder structure according to their prim path. When disabled,
assets are imported into content folders according to asset type (e.g. ‘Materials’, ‘StaticMeshes’, etc).

- `prims_to_import` (Array[str]): [Read-Write] List of paths of prims to import (e.g. [“/Root/MyBox”, “/Root/OtherPrim”]).
Importing a prim will import its entire subtree.
If this list contains the root prim path the entire stage will be imported (default value).

- `purposes_to_import` (int32): [Read-Write] Only import prims with these specific purposes from the USD file

- `render_context_to_import` (Name): [Read-Write] Specifies which set of shaders to use when parsing USD materials, in addition to the universal render context.

- `root_motion_handling` (UsdRootMotionHandling): [Read-Write] Describes what to add to the root bone animation within generated AnimSequences, if anything

- `share_assets_for_identical_prims` (bool): [Read-Write] If true, whenever two prims would have generated identical UAssets (like identical StaticMeshes or materials) then only one instance of
that asset is generated, and the asset is shared by the components generated for both prims.
If false, we will always generate a dedicated asset for each prim.

- `stage_options` (UsdStageOptions): [Read-Write] Custom StageOptions to use for the stage

- `subdivision_level` (int32): [Read-Write] Subdivision level to use for all subdivision meshes on the opened stage. 0 means “don’t subdivide”

- `use_existing_asset_cache` (bool): [Read-Write]

- `use_prim_kinds_for_collapsing` (bool): [Read-Write] Use KindsToCollapse to determine when to collapse prim subtrees or not (defaults to enabled).
Disable this if you want to prevent collapsing, or to control it manually by right-clicking on individual prims.



---

_property_ `existing_actor_policy`: ReplaceActorPolicy

[Read-Write] What should happen when imported actors and components try to overwrite existing actors and components

**Type:**

( ReplaceActorPolicy)


---

_property_ `existing_asset_cache`: SoftObjectPath

[Read-Write] Copy assets from an existing UsdAsset cache instead of generating them from scratch, if possible

**Type:**

( SoftObjectPath)


---

_property_ `existing_asset_policy`: ReplaceAssetPolicy

[Read-Write] What should happen when imported assets try to overwrite existing assets

**Type:**

( ReplaceAssetPolicy)


---

_property_ `fallback_collision_type`: UsdCollisionType

[Read-Write] What type of collision to use for static meshes generated from Prims that don’t have physics schemas applied

**Type:**

( UsdCollisionType)


---

_property_ `groom_interpolation_settings`: None

[Read-Write] Groom group interpolation settings

**Type:**

( Array\ [HairGroupsInterpolation])


---

_property_ `import_actors`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `import_at_specific_time_code`: bool

[Read-Write] When true the stage will be evaluated at ImportTimeCode for the import.
When false, the stage will be evaluated at the default (non-animated) timecode

**Type:**

( bool)


---

_property_ `import_geometry`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `import_groom_assets`: bool

[Read-Write] Whether to import GroomAssets, GroomCaches and GroomBindings

**Type:**

( bool)


---

_property_ `import_level_sequences`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `import_materials`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `import_only_used_materials`: bool

[Read-Write] If this is checked, only materials actively used by the stage and import settings will be parsed.
If this is unchecked, all materials present on the stage will be parsed.

**Type:**

( bool)


---

_property_ `import_skeletal_animations`: bool

[Read-Write] Whether to try importing UAnimSequence skeletal animation assets for each encountered UsdSkelAnimQuery

**Type:**

( bool)


---

_property_ `import_sounds`: bool

[Read-Write] Whether to import audio files referenced by UsdMediaSpatialAudio schemas as Unreal sound assets

**Type:**

( bool)


---

_property_ `import_sparse_volume_textures`: bool

[Read-Write] Whether to import OpenVDB volumes as Sparse Volume Textures

**Type:**

( bool)


---

_property_ `import_time_code`: float

[Read-Write] TimeCode to evaluate the stage for import, in case bImportAtSpecificTimeCode is enabled

**Type:**

( float)


---

_property_ `interpret_lo_ds`: bool

‘interpret\_lo\_ds’ was renamed to ‘interpret\_lods’.

**Type:**

deprecated


---

_property_ `interpret_lods`: bool

[Read-Write] When true, if a prim has a “LOD” variant set with variants named “LOD0”, “LOD1”, etc. where each contains a UsdGeomMesh, the importer will
attempt to parse the meshes as separate LODs of a single UStaticMesh. When false, only the selected variant will be parsed as LOD0 of the
UStaticMesh.

**Type:**

( bool)


---

_property_ `kinds_to_collapse`: int

[Read-Write] Whether to try to combine individual assets and components of the same type on a kind-per-kind basis,
like multiple Mesh prims into a single Static Mesh

**Type:**

(int32)


---

_property_ `material_purpose`: Name

[Read-Write] Specifies which material purpose to use when parsing USD material bindings, in addition to the “allPurpose” fallback

**Type:**

( Name)


---

_property_ `merge_identical_material_slots`: bool

[Read-Write] Identical material slots will be combined into a single slot if this is enabled. This is only performed in the context
of mesh collapsing, or when parsing LOD variant sets (see bInterpretLODs)

**Type:**

( bool)


---

_property_ `metadata_options`: UsdMetadataImportOptions

[Read-Write] Describes if/how we should collect metadata from USD prims onto the assets and components we generate when importing

**Type:**

( UsdMetadataImportOptions)


---

_property_ `nanite_triangle_threshold`: int

[Read-Write] Try enabling Nanite for static meshes that are generated with at least this many triangles

**Type:**

(int32)


---

_property_ `override_stage_options`: bool

[Read-Write] Whether to use the specified StageOptions instead of the stage’s own settings

**Type:**

( bool)


---

_property_ `prim_path_folder_structure`: bool

[Read-Write] When enabled, assets will be imported into a content folder structure according to their prim path. When disabled,
assets are imported into content folders according to asset type (e.g. ‘Materials’, ‘StaticMeshes’, etc).

**Type:**

( bool)


---

_property_ `prims_to_import`: None

[Read-Write] List of paths of prims to import (e.g. [“/Root/MyBox”, “/Root/OtherPrim”]).
Importing a prim will import its entire subtree.
If this list contains the root prim path the entire stage will be imported (default value).

**Type:**

( Array\ [str])


---

_property_ `purposes_to_import`: int

[Read-Write] Only import prims with these specific purposes from the USD file

**Type:**

(int32)


---

_property_ `render_context_to_import`: Name

[Read-Write] Specifies which set of shaders to use when parsing USD materials, in addition to the universal render context.

**Type:**

( Name)


---

_property_ `root_motion_handling`: UsdRootMotionHandling

[Read-Write] Describes what to add to the root bone animation within generated AnimSequences, if anything

**Type:**

( UsdRootMotionHandling)


---

_property_ `share_assets_for_identical_prims`: bool

[Read-Write] If true, whenever two prims would have generated identical UAssets (like identical StaticMeshes or materials) then only one instance of
that asset is generated, and the asset is shared by the components generated for both prims.
If false, we will always generate a dedicated asset for each prim.

**Type:**

( bool)


---

_property_ `stage_options`: UsdStageOptions

[Read-Write] Custom StageOptions to use for the stage

**Type:**

( UsdStageOptions)


---

_property_ `subdivision_level`: int

[Read-Write] Subdivision level to use for all subdivision meshes on the opened stage. 0 means “don’t subdivide”

**Type:**

(int32)


---

_property_ `use_existing_asset_cache`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `use_prim_kinds_for_collapsing`: bool

[Read-Write] Use KindsToCollapse to determine when to collapse prim subtrees or not (defaults to enabled).
Disable this if you want to prevent collapsing, or to control it manually by right-clicking on individual prims.

**Type:**

( bool)

### Table of Contents

- `unreal.UsdStageImportOptions`
  - `UsdStageImportOptions`
    - `UsdStageImportOptions.existing_actor_policy`
    - `UsdStageImportOptions.existing_asset_cache`
    - `UsdStageImportOptions.existing_asset_policy`
    - `UsdStageImportOptions.fallback_collision_type`
    - `UsdStageImportOptions.groom_interpolation_settings`
    - `UsdStageImportOptions.import_actors`
    - `UsdStageImportOptions.import_at_specific_time_code`
    - `UsdStageImportOptions.import_geometry`
    - `UsdStageImportOptions.import_groom_assets`
    - `UsdStageImportOptions.import_level_sequences`
    - `UsdStageImportOptions.import_materials`
    - `UsdStageImportOptions.import_only_used_materials`
    - `UsdStageImportOptions.import_skeletal_animations`
    - `UsdStageImportOptions.import_sounds`
    - `UsdStageImportOptions.import_sparse_volume_textures`
    - `UsdStageImportOptions.import_time_code`
    - `UsdStageImportOptions.interpret_lo_ds`
    - `UsdStageImportOptions.interpret_lods`
    - `UsdStageImportOptions.kinds_to_collapse`
    - `UsdStageImportOptions.material_purpose`
    - `UsdStageImportOptions.merge_identical_material_slots`
    - `UsdStageImportOptions.metadata_options`
    - `UsdStageImportOptions.nanite_triangle_threshold`
    - `UsdStageImportOptions.override_stage_options`
    - `UsdStageImportOptions.prim_path_folder_structure`
    - `UsdStageImportOptions.prims_to_import`
    - `UsdStageImportOptions.purposes_to_import`
    - `UsdStageImportOptions.render_context_to_import`
    - `UsdStageImportOptions.root_motion_handling`
    - `UsdStageImportOptions.share_assets_for_identical_prims`
    - `UsdStageImportOptions.stage_options`
    - `UsdStageImportOptions.subdivision_level`
    - `UsdStageImportOptions.use_existing_asset_cache`
    - `UsdStageImportOptions.use_prim_kinds_for_collapsing`
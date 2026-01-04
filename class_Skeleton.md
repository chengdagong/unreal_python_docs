# unreal.Skeleton

```python
class unreal.Skeleton(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


USkeletonthat links between mesh and animation

- Bone hierarchy for animations

- Bone/track linkup between mesh and animation

- Retargetting related


**C++ Source:**

- **Module**: Engine

- **File**: Skeleton.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the asset

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the asset

- `bone_tree` (Array[BoneNode]): [Read-Only] Skeleton bone tree - each contains name and parent index\*

- `compatible_skeletons` (Array[Skeleton]): [Read-Write] The list of compatible skeletons. This skeleton will be able to use animation data originating from skeletons within this array, such as animation sequences.
This property is not bi-directional.

This is an array of TSoftObjectPtr in order to prevent all skeletons to be loaded, as we only want to load things on demand.
As this is EditAnywhere and an array of TSoftObjectPtr, checking validity of pointers is needed.

- `preview_forward_axis` (AxisType): [Read-Write] Preview axis to consider as “forward” for the skeleton. Only used for preview purposes.

- `use_retarget_modes_from_compatible_skeleton` (bool): [Read-Write] Should we use the per bone translational retarget mode from the source (compatible) skeleton’s instead of from this skeleton? On default this is disabled.
Enabling this would allow you to have one shared set of animations. You would configure the retarget settings on the animation skeleton.
Then every character that plays animations from this source skeleton will use the translational retarget settings from the source skeleton, which saves you from
having to configure the retarget modes for every bone in every character as they can be setup just once now on the animation skeleton.



---

**add_asset_user_data_of_class**( _user_data_class_) → `bool`

Creates and adds an instance of the provided AssetUserData class to the target asset.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to create

Returns:

Whether or not an instance of InUserDataClass was succesfully added

Return type:

bool


---

**add_compatible_skeleton**( _source_skeleton_) → `None`

Add Compatible Skeleton

Parameters:

**source\_skeleton** ( _Skeleton_)


---

**add_compatible_skeleton_soft**( _source_skeleton_) → `None`

Add Compatible Skeleton Soft

Parameters:

**source\_skeleton** ( _Skeleton_)


---

**add_curve_meta_data**( _curve_name_, _transact=True_) → `bool`

Adds a curve metadata entry with the specified name on the skeleton

Parameters:

- **curve\_name** ( _Name_)

- **transact** ( _bool_) – If true record a new transaction


Returns:

true if an entry was added, false if an entry already existed

Return type:

bool


---

_property_ `compatible_skeletons`: None

[Read-Only] The list of compatible skeletons. This skeleton will be able to use animation data originating from skeletons within this array, such as animation sequences.
This property is not bi-directional.

This is an array of TSoftObjectPtr in order to prevent all skeletons to be loaded, as we only want to load things on demand.
As this is EditAnywhere and an array of TSoftObjectPtr, checking validity of pointers is needed.

**Type:**

( Array\ [Skeleton])


---

**copy_bones_from_skeleton**( _target_mesh_, _options=[False, BonesToCopyFromSource.ALL_BONES]_, _debug=None_) → `DynamicMesh`

Copy the bone attributes (skeleton) from the SourceSkeleton to the TargetMesh.

Parameters:

- **target\_mesh** ( _DynamicMesh_) – Mesh we are copying the bone attributes to.

- **options** ( _GeometryScriptCopyBonesFromMeshOptions_) – An option object to control how the copying is performed.

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

**find_curve_identifier**( _name_, _curve_type_) → `AnimationCurveIdentifier`

Tries to construct a valid FAnimationCurveIdentifier instance. It tries to find the underlying SmartName on the provided Skeleton for the provided curve type.
deprecated: Curve identifiers are no longer retrievable globally from the skeleton, they are specified per-animation.

Parameters:

- **name** ( _Name_) – Name of the curve to find

- **curve\_type** ( _RawCurveTrackTypes_) – Type of the curve to find


Returns:

Valid FAnimationCurveIdentifier if the name exists on the skeleton and the operation was successful, invalid otherwise

Return type:

AnimationCurveIdentifier


---

**get_asset_user_data_of_class**( _user_data_class_) → `AssetUserData`

Returns an instance of the provided AssetUserData class if it’s contained in the target asset.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to get

Returns:

The instance of the UAssetUserData class contained, or null if it doesn’t exist

Return type:

AssetUserData


---

**get_blend_profile**( _profile_name_) → `BlendProfile`

Get the specified blend profile by name

Parameters:

**profile\_name** ( _Name_)

Return type:

BlendProfile


---

**get_curve_identifier**( _name_, _curve_type_) → `AnimationCurveIdentifier`

Get Curve Identifier
deprecated: Please use SetCurveIdentifier.

Parameters:

- **name** ( _Name_)

- **curve\_type** ( _RawCurveTrackTypes_)


Return type:

AnimationCurveIdentifier


---

**get_curve_identifiers**( _curve_type_) → `Array\ [AnimationCurveIdentifier]`

Retrieves all curve identifiers for a specific curve types from the provided Skeleton
deprecated: Curve identifiers are no longer retrievable globally from the skeleton, they are specified per-animation.

Parameters:

**curve\_type** ( _RawCurveTrackTypes_) – Type of the curve identifers to retrieve

Returns:

Array of FAnimationCurveIdentifier instances each representing a unique curve if the operation was successful, empyty array otherwise

Return type:

Array\ [AnimationCurveIdentifier]


---

**get_curve_meta_data_material**( _curve_name_) → `bool`

Gets the material flag for a curve’s metadata

Parameters:

**curve\_name** ( _Name_) – The name of the curve to check

Returns:

true if the flag has been set

Return type:

bool


---

**get_curve_meta_data_morph_target**( _curve_name_) → `bool`

Gets the morph target flag for a curve’s metadata

Parameters:

**curve\_name** ( _Name_) – The name of the curve to check

Returns:

true if the flag has been set

Return type:

bool


---

**get_curve_meta_data_names**() → `Array\ [Name]`

Get an array of all curve metadata names

Returns:

out\_names (Array[Name]): The array to receive the metadata names

Return type:

Array\ [Name]


---

**get_num_curve_meta_data**() → `int32Returns:`

the number of curve metadata entries on the skeleton \*

Return type:

int32


---

**get_reference_pose**() → `AnimPose`

Populates an Anim Pose with the reference poses stored for the provided USkeleton

Returns:

out\_pose (AnimPose): Anim pose to hold the reference pose

Return type:

AnimPose


---

**has_asset_user_data_of_class**( _user_data_class_) → `bool`

Checks whether or not an instance of the provided AssetUserData class is contained.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to check for

Returns:

Whether or not an instance of InUserDataClass was found

Return type:

bool


---

**remove_curve_meta_data**( _curve_name_) → `bool`

Removes a curve metadata entry for the specified name.

Parameters:

**curve\_name** ( _Name_) – The name of the curve to remove the metadata for

Returns:

true if the entry was successfully removed (i.e. it existed)

Return type:

bool


---

**rename_curve_meta_data**( _old_name_, _new_name_) → `bool`

Renames a curve metadata entry. Metadata is preserved, but assigned to a different curve name.

Parameters:

- **old\_name** ( _Name_) – The name of an existing curve entry

- **new\_name** ( _Name_) – The name to change the entry to


Returns:

true if the rename was successful (the old name was found and the new name didnt collide with an existing entry)

Return type:

bool


---

**set_curve_meta_data_material**( _curve_name_, _override_material_) → `None`

Set the material flag for a curve’s metadata

Parameters:

- **curve\_name** ( _Name_) – The name of the curve to set

- **override\_material** ( _bool_) – Whether to set the material flag



---

**set_curve_meta_data_morph_target**( _curve_name_, _override_morph_target_) → `None`

Set the morph target flag for a curve’s metadata

Parameters:

- **curve\_name** ( _Name_) – The name of the curve to set

- **override\_morph\_target** ( _bool_) – Whether to set the morph target flag


### Table of Contents

- `unreal.Skeleton`
  - `Skeleton`
    - `Skeleton.add_asset_user_data_of_class()`
    - `Skeleton.add_compatible_skeleton()`
    - `Skeleton.add_compatible_skeleton_soft()`
    - `Skeleton.add_curve_meta_data()`
    - `Skeleton.compatible_skeletons`
    - `Skeleton.copy_bones_from_skeleton()`
    - `Skeleton.find_curve_identifier()`
    - `Skeleton.get_asset_user_data_of_class()`
    - `Skeleton.get_blend_profile()`
    - `Skeleton.get_curve_identifier()`
    - `Skeleton.get_curve_identifiers()`
    - `Skeleton.get_curve_meta_data_material()`
    - `Skeleton.get_curve_meta_data_morph_target()`
    - `Skeleton.get_curve_meta_data_names()`
    - `Skeleton.get_num_curve_meta_data()`
    - `Skeleton.get_reference_pose()`
    - `Skeleton.has_asset_user_data_of_class()`
    - `Skeleton.remove_curve_meta_data()`
    - `Skeleton.rename_curve_meta_data()`
    - `Skeleton.set_curve_meta_data_material()`
    - `Skeleton.set_curve_meta_data_morph_target()`
# unreal.AnimMontage

```python
class unreal.AnimMontage(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``AnimCompositeBase``


Any property you’re adding to AnimMontage and parent class has to be considered for Child Asset

Child Asset is considered to be only asset mapping feature using everything else in the class
For example, you can just use all parent’s setting for the montage, but only remap assets
This isn’t magic bullet unfortunately and it is consistent effort of keeping the data synced with parent
If you add new property, please make sure those property has to be copied for children.
If it does, please add the copy in the function RefreshParentAssetData

**C++ Source:**

- **Module**: Engine

- **File**: AnimMontage.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_mapping_table` (AssetMappingTable): [Read-Only] Asset mapping table when ParentAsset is set

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the asset

- `blend_in` (AlphaBlend): [Read-Write] Blend in option.

- `blend_mode_in` (MontageBlendMode): [Read-Write]

- `blend_mode_out` (MontageBlendMode): [Read-Write]

- `blend_out` (AlphaBlend): [Read-Write] Blend out option. This is only used when it blends out itself. If it’s interrupted by other montages, it will use new montage’s BlendIn option to blend out.

- `blend_out_trigger_time` (float): [Read-Write] Time from Sequence End to trigger blend out.
<0 means using BlendOutTime, so BlendOut finishes as Montage ends.
>=0 means using ‘SequenceEnd - BlendOutTriggerTime’ to trigger blend out.

- `blend_profile_in` (BlendProfile): [Read-Write] The blend profile to use.

- `blend_profile_out` (BlendProfile): [Read-Write] The blend profile to use.

- `common_target_frame_rate` (FrameRate): [Read-Only] Frame-rate used to represent this Animation Montage (best fitting for placed Animation Sequences)

- `controller` (AnimationDataController): [Read-Only] UAnimDataController instance set to operate on DataModel

- `data_model` (AnimDataModel): [Read-Only]

- `data_model_interface` (AnimationDataModel): [Read-Only] IAnimationDataModel instance containing (source) animation data

- `enable_auto_blend_out` (bool): [Read-Write] When it hits end, it automatically blends out. If this is false, it won’t blend out but keep the last pose until stopped explicitly

- `loop` (bool): [Read-Write] The default looping behavior of this animation.
Asset players can override this

- `meta_data` (Array[AnimMetaData]): [Read-Write] Meta data that can be saved with the asset

You can query by GetMetaData function

- `parent_asset` (AnimationAsset): [Read-Only] Parent Asset, if set, you won’t be able to edit any data in here but just mapping table

During cooking, this data will be used to bake out to normal asset

- `preview_base_pose` (AnimSequence): [Read-Write] Preview Base pose for additive BlendSpace \*

- `preview_pose_asset` (PoseAsset): [Read-Write] The default skeletal mesh to use when previewing this asset - this only applies when you open Persona using this asset//
todo:: note that this doesn’t retarget right now

- `rate_scale` (float): [Read-Write] Number for tweaking playback rate of this animation globally.

- `sequence_length` (float): [Read-Only]

- `skeleton` (Skeleton): [Read-Only] Pointer to the Skeleton this asset can be played on .

- `sync_group` (Name): [Read-Write] If you’re using marker based sync for this montage, make sure to add sync group name. For now we only support one group

- `sync_slot_index` (int32): [Read-Write] Index of the slot track used for collecting sync markers

- `thumbnail_info` (ThumbnailInfo): [Read-Only] Information for thumbnail rendering

- `time_stretch_curve` (TimeStretchCurve): [Read-Write] Time stretch curve will only be used when the montage has a non-default play rate

- `time_stretch_curve_name` (Name): [Read-Write] Name of optional TimeStretchCurveName to look for in Montage. Time stretch curve will only be used when the montage has a non-default play rate



---

_property_ `blend_mode_in`: MontageBlendMode

[Read-Only]

**Type:**

( MontageBlendMode)


---

_property_ `blend_mode_out`: MontageBlendMode

[Read-Only]

**Type:**

( MontageBlendMode)


---

_property_ `blend_profile_in`: BlendProfile

[Read-Only] The blend profile to use.

**Type:**

( BlendProfile)


---

_property_ `blend_profile_out`: BlendProfile

[Read-Only] The blend profile to use.

**Type:**

( BlendProfile)


---

_classmethod_ create_slot_animation_as_dynamic_montage_with_blend_settings( _asset_, _slot_node_name_, _blend_in_settings_, _blend_out_settings_, _play_rate=1.000000_, _loop_count=1_, _blend_out_trigger_time=-1.000000_)→AnimMontage

Utility function to create dynamic montage from AnimSequence with blend in settings

Parameters:

- **asset** ( _AnimSequenceBase_)

- **slot\_node\_name** ( _Name_)

- **blend\_in\_settings** ( _MontageBlendSettings_)

- **blend\_out\_settings** ( _MontageBlendSettings_)

- **play\_rate** ( _float_)

- **loop\_count** ( _int32_)

- **blend\_out\_trigger\_time** ( _float_)


Return type:

AnimMontage


---

**get_blend_in_args**() → `AlphaBlendArgs`

Get Blend in Args

Return type:

AlphaBlendArgs


---

**get_blend_out_args**() → `AlphaBlendArgs`

Get Blend Out Args

Return type:

AlphaBlendArgs


---

**get_default_blend_in_time**() → `float`

Get Default Blend in Time

Return type:

float


---

**get_default_blend_out_time**() → `float`

Get Default Blend Out Time

Return type:

float


---

**get_first_anim_reference**() → `AnimSequenceBase`

Get First Anim Reference

Return type:

AnimSequenceBase


---

**get_group_name**() → `Name`

Get the Montage’s Group Name. This is the group from the first slot.

Return type:

Name


---

**get_num_sections**() → `int32`

Returns the number of sections this montage has

Return type:

int32


---

**get_section_index**( _section_name_) → `int32`

Get SectionIndex from SectionName. Returns INDEX\_None if not found

Parameters:

**section\_name** ( _Name_)

Return type:

int32


---

**get_section_name**( _section_index_) → `Name`

Get SectionName from SectionIndex. Returns NAME\_None if not found

Parameters:

**section\_index** ( _int32_)

Return type:

Name


---

**is_dynamic_montage**() → `bool`

Is Dynamic Montage

Return type:

bool


---

**is_valid_additive_slot**( _slot_node_name_) → `bool`

Check if this slot has a valid additive animation for the specified slot.
The slot name should not include the group name.
i.e. for “DefaultGroup.DefaultSlot”, the slot name is “DefaultSlot”.

Parameters:

**slot\_node\_name** ( _Name_)

Return type:

bool


---

**is_valid_section_name**( _section_name_) → `boolParameters:`

**section\_name** ( _Name_)

Returns:

true if valid section

Return type:

bool

### Table of Contents

- `unreal.AnimMontage`
  - `AnimMontage`
    - `AnimMontage.blend_mode_in`
    - `AnimMontage.blend_mode_out`
    - `AnimMontage.blend_profile_in`
    - `AnimMontage.blend_profile_out`
    - `AnimMontage.create_slot_animation_as_dynamic_montage_with_blend_settings()`
    - `AnimMontage.get_blend_in_args()`
    - `AnimMontage.get_blend_out_args()`
    - `AnimMontage.get_default_blend_in_time()`
    - `AnimMontage.get_default_blend_out_time()`
    - `AnimMontage.get_first_anim_reference()`
    - `AnimMontage.get_group_name()`
    - `AnimMontage.get_num_sections()`
    - `AnimMontage.get_section_index()`
    - `AnimMontage.get_section_name()`
    - `AnimMontage.is_dynamic_montage()`
    - `AnimMontage.is_valid_additive_slot()`
    - `AnimMontage.is_valid_section_name()`
# unreal.StreamableSparseVolumeTexture

```python
class unreal.StreamableSparseVolumeTexture(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SparseVolumeTexture``


Represents a streamable SparseVolumeTexture asset and serves as base class for UStaticSparseVolumeTexture and UAnimatedSparseVolumeTexture. It has an array of USparseVolumeTextureFrame.

**C++ Source:**

- **Module**: Engine

- **File**: SparseVolumeTexture.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `address_x` (TextureAddress): [Read-Write] The addressing mode to use for the X axis.

- `address_y` (TextureAddress): [Read-Write] The addressing mode to use for the Y axis.

- `address_z` (TextureAddress): [Read-Write] The addressing mode to use for the Z axis.

- `asset_import_data` (AssetImportData): [Read-Only]

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the asset

- `fallback_value_a` (Vector4f): [Read-Only]

- `fallback_value_b` (Vector4f): [Read-Only]

- `format_a` (PixelFormat): [Read-Only]

- `format_b` (PixelFormat): [Read-Only]

- `local_ddc_only` (bool): [Read-Write] If enabled, the SparseVolumeTexture is only going to use the local DDC. For certain assets it might be reasonable to also use the remote DDC, but for larger assets this will mean long up- and download times.

- `num_frames` (int32): [Read-Only]

- `num_mip_levels` (int32): [Read-Only]

- `number_of_prefetch_frames` (int32): [Read-Write] When using non-blocking streaming requests, upcoming frames are loaded into memory in advance. This property controls how many frames to prefetch.

- `prefetch_percentage_bias` (float): [Read-Write] When using non-blocking streaming requests, upcoming frames are loaded into memory in advance. This property applies a bias in percent to how much data is prefetched for every frame.
A value of 20.0 adds 20% to all prefetch percentages. So if PrefetchPercentageStepSize is set to 20.0, frame N+1 is prefetched at 80% + 20% = 100%, frame N+2 at 60% + 20% = 80%, N+3 at 40% + 20% = 60% etc.

- `prefetch_percentage_step_size` (float): [Read-Write] When using non-blocking streaming requests, upcoming frames are loaded into memory in advance. This property controls the size reduction in percent of each additional prefetched frames.
A value of 20.0 would prefetch frame N+1 at 80%, N+2 at 60%, N+3 at 40% etc.

- `streaming_pool_size_factor` (float): [Read-Write] The SVT streaming pool is sized such that it can hold the largest frame multiplied by this value. There should be some slack to allow for prefetching frames.

- `volume_resolution` (IntVector): [Read-Only]



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

_property_ `address_x`: TextureAddress

[Read-Write] The addressing mode to use for the X axis.

**Type:**

( TextureAddress)


---

_property_ `address_y`: TextureAddress

[Read-Write] The addressing mode to use for the Y axis.

**Type:**

( TextureAddress)


---

_property_ `address_z`: TextureAddress

[Read-Write] The addressing mode to use for the Z axis.

**Type:**

( TextureAddress)


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

**has_asset_user_data_of_class**( _user_data_class_) → `bool`

Checks whether or not an instance of the provided AssetUserData class is contained.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to check for

Returns:

Whether or not an instance of InUserDataClass was found

Return type:

bool


---

_property_ `local_ddc_only`: bool

[Read-Write] If enabled, the SparseVolumeTexture is only going to use the local DDC. For certain assets it might be reasonable to also use the remote DDC, but for larger assets this will mean long up- and download times.

**Type:**

( bool)

### Table of Contents

- `unreal.StreamableSparseVolumeTexture`
  - `StreamableSparseVolumeTexture`
    - `StreamableSparseVolumeTexture.add_asset_user_data_of_class()`
    - `StreamableSparseVolumeTexture.address_x`
    - `StreamableSparseVolumeTexture.address_y`
    - `StreamableSparseVolumeTexture.address_z`
    - `StreamableSparseVolumeTexture.get_asset_user_data_of_class()`
    - `StreamableSparseVolumeTexture.has_asset_user_data_of_class()`
    - `StreamableSparseVolumeTexture.local_ddc_only`
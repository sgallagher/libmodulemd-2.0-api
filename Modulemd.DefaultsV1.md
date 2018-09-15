# Modulemd.DefaultsV1 ([Modulemd.Defaults](Modulemd.Defaults.md))
Defaults for modules

## Properties

__version__: (ro) (uint64) The metadata version of this Defaults object. Defaults to the highest-supported version if not specified at object construction. Cannot be changed after object construction except through the upgrade() routine.

__module_name__: (ro) (string) The name of the module to which these defaults apply.

__default_stream__: (rw) (string) (nullable) The default stream for the module

__intent__: (rw) (nullable) The system intent these defaults apply to. If unspecified, these are general defaults.


## Public Methods

---
### new()

#### Arguments:
__version__: (in) (uint64) The version of the Defaults metadata.

__module_name__: (in) (string) The name of the module to which these defaults apply.

#### Returns:
([Modulemd.DefaultsV1](Modulemd.DefaultsV1.md)) (transfer full) A newly-allocated Modulemd.DefaultsV1 object.

---
### upgrade()
Upgrade this version of the defaults metadata to a newer version.

#### Arguments:
__self__: (in) ([Modulemd.DefaultsV1](Modulemd.DefaultsV1.md)) This [Modulemd.DefaultsV1](Modulemd.DefaultsV1.md) object.

__target_version__: (in) (uint64) The version to upgrade to. Must be higher than the current version.

__error__: (out) (GError) A GError containing the reason the object failed to upgrade, NULL if the upgrade succeeded.


#### Returns:
(bool) TRUE if the upgrade succeeded. If the upgrade could not complete, returns FALSE and sets `error` appropriately.

---
### get_version()
Gets the numeric version associated with this object. This will never be modified after object construction.

#### Arguments:
__self__: (in) ([Modulemd.DefaultsV1](Modulemd.DefaultsV1.md)) This [Modulemd.DefaultsV1](Modulemd.DefaultsV1.md) object.

#### Returns:
(uint64) The metadata version represented by this [Modulemd.DefaultsV1](Modulemd.DefaultsV1.md) object.

---
### set_module_name()
Sets the module name. This should normally be done during object creation and remain unchanged. This object will fail validation if `module_name` is unset.

#### Arguments:
__self__: (in) ([Modulemd.DefaultsV1](Modulemd.DefaultsV1.md)) This [Modulemd.DefaultsV1](Modulemd.DefaultsV1.md) object.

__module_name__: (in) (string) The name of the module to which these defaults apply.

#### Returns:
(void)

---
### get_module_name()
#### Arguments:
__self__: (in) ([Modulemd.DefaultsV1](Modulemd.DefaultsV1.md)) This [Modulemd.DefaultsV1](Modulemd.DefaultsV1.md) object.

#### Returns:
(string) (transfer none) The name of the module to which these defaults apply.

---
### set_default_stream()
#### Arguments
__self__: (in) ([Modulemd.DefaultsV1V1](Modulemd.DefaultsV1V1.md)) This [Modulemd.DefaultsV1V1](Modulemd.DefaultsV1V1.md) object.

__default_stream: (in) (string) The name of the default stream for this module.

#### Returns:
(void)

---
### get_default_stream()
#### Arguments
__self__: (in) ([Modulemd.DefaultsV1V1](Modulemd.DefaultsV1V1.md)) This [Modulemd.DefaultsV1V1](Modulemd.DefaultsV1V1.md) object.

#### Returns:
(string) (transfer none) The name of the default stream for this module.

---
### get_streams_with_default_profiles_as_strv()
Gets a list of streams that have had default profiles set for this module.

#### Arguments:
__self__: (in) ([Modulemd.DefaultsV1V1](Modulemd.DefaultsV1V1.md)) This [Modulemd.DefaultsV1V1](Modulemd.DefaultsV1V1.md) object.

#### Returns:
(strv) (transfer full) A sorted list of unique stream names for which default profiles have been assigned.

---
### add_default_profile_for_stream()
Add a profile that will be installed for this stream if none are explicitly specified by the user.

This function may be called any number of times for the same stream and will deduplicate input.

#### Arguments:
__self__: (in) ([Modulemd.DefaultsV1V1](Modulemd.DefaultsV1V1.md)) This [Modulemd.DefaultsV1V1](Modulemd.DefaultsV1V1.md) object.

__stream__: (in) (string): The name of the module stream to which to add this default profile.

__profile__: (in) (string): The name of the default profile to add.

#### Returns:
(void)

---
### remove_default_profiles_for_stream()
Remove all default profiles for the specified stream.

#### Arguments:
__self__: (in) ([Modulemd.DefaultsV1V1](Modulemd.DefaultsV1V1.md)) This [Modulemd.DefaultsV1V1](Modulemd.DefaultsV1V1.md) object.

#### Returns:
(void)

---
### get_default_profiles_for_stream_as_strv()
Returns a sorted, deduplicated list of the default profiles for the specified stream.

#### Arguments:
__self__: (in) ([Modulemd.DefaultsV1V1](Modulemd.DefaultsV1V1.md)) This [Modulemd.DefaultsV1V1](Modulemd.DefaultsV1V1.md) object.

__stream__: (in) (string) The name of the string to retrieve default profiles for.

#### Returns:
(strv) (transfer full) A sorted list of unique profiles to be installed by default for this stream.

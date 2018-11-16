# Modulemd.DefaultsV1 ([Modulemd.Defaults](Modulemd.Defaults.md))
Defaults for modules

## Properties

__default_stream__: (rw) (string) (nullable) The default stream for the module

__intent__: (rw) (nullable) The system intent these defaults apply to. If unspecified, these are general defaults.


## Public Methods

---
### new()

#### Arguments:
__module_name__: (in) (string) The name of the module to which these defaults apply.

#### Returns:
([Modulemd.DefaultsV1](Modulemd.DefaultsV1.md)) (transfer full) A newly-allocated Modulemd.DefaultsV1 object.

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

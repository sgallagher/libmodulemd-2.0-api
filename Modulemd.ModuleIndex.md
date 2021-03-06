# Modulemd.ModuleIndex(GObject)
A simplistic wrapper around GHashTable to ensure type-safety for [Modulemd.Module](Modulemd.Module.md) objects.

## Properties

## Public Methods

---
### new()
#### Arguments:
#### Returns:
([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md)) (transfer full) A newly-allocated [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object.

---
### update_from_file()
#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

__yaml_file__: (in) (string) A YAML file containing the module metadata and other related information such as default streams.

__failures__: (out) (list<[Modulemd.Subdocument](Modulemd.Subdocument.md)>) An array containing any subdocuments from the YAML file that failed to parse. See [Modulemd.Subdocument](Modulemd.Subdocument.md) for more details.

__error__: (out) (GError) A GError containing additional information if this function fails.

#### Returns:
(bool) Returns TRUE if the update was successful. Returns FALSE and sets `failures` and `error` appropriately if any of the YAML subdocuments were invalid or there was a parser error.

---
### update_from_string()
#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

__yaml_string__: (in) (string) A YAML string containing the module metadata and other related information such as default streams.

__failures__: (out) (list<[Modulemd.Subdocument](Modulemd.Subdocument.md)>) An array containing any subdocuments from the YAML file that failed to parse. See [Modulemd.Subdocument](Modulemd.Subdocument.md) for more details.

__error__: (out) (GError) A GError containing additional information if this function completely fails.

#### Returns:
([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md)) (transfer full) An object containing all [Modulemd.Module](Modulemd.Module.md) objects (including defaults and translations) included in this YAML stream, indexed by the module name.

---
### update_from_stream()
#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

__yaml_stream__: (in) (string) 	
A YAML stream containing the module metadata and other related information such as default streams.

__failures__: (out) (list<[Modulemd.Subdocument](Modulemd.Subdocument.md)>) An array containing any subdocuments from the YAML file that failed to parse. See [Modulemd.Subdocument](Modulemd.Subdocument.md) for more details.

__error__: (out) (GError) A GError containing additional information if this function completely fails.

#### Returns:
(bool) Returns TRUE if the update was successful. Returns FALSE and sets `failures` and `error` appropriately if any of the YAML subdocuments were invalid or there was a parser error.

---
### dump_yaml_file()
#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

__yaml_file__: (in) (string) The path to the file that should contain the resulting YAML.

__error__: (out) (GError) A GError containing the reason the function failed, NULL if the function succeeded.

#### Returns:
(bool) TRUE if the file was written successfully. In the event of an error, sets `error` appropriately and returns FALSE.

---
### dump_yaml_string()
#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

__error__: (out) (GError) A GError containing the reason the function failed, NULL if the function succeeded.

#### Returns:
(string) (transfer full) A YAML representation of the index as a string. In the event of an error, sets `error` appropriately and returns NULL.

---
### validate()
This method ensures that all objects in the index are internally consistent for usage or dumping to YAML. It will be run implicitly prior to emitting YAML. This is *not* a complete linter, merely a sanity check that the values are not impossible.

#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

__error__: (out) (GError) A GError containing the reason the object failed validation, NULL if the validation passed.

#### Returns:
(bool) TRUE if validation passed.

---
### get_module_names_as_strv()
#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

#### Returns:
(GStrv) (transfer full) An ordered list of string keys in this index.

---
### get_module()
#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

__module_name__: (in) (string) The module name to look up in the index.

#### Returns:
([Modulemd.Module](Modulemd.Module.md)) (transfer none) The [Modulemd.Module](Modulemd.Module.md) object matching the provided module name or NULL if the key was not present in the index.

---
### add_module()
#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

__module__: (in) The [Modulemd.Module](Modulemd.Module.md) object to add to the index.

__error__: (out) (GError) A GError containing the reason the [Modulemd.Module](Modulemd.Module.md) object could not be added or NULL if the function succeeded.

#### Returns:
(bool) TRUE if the [Modulemd.Module](Modulemd.Module.md) object was added successfully. If the module name already existed in the index, it will be replaced by this one. On failure, returns FALSE and sets `error` appropriately.

---
### remove_module()
#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

__module_name__: (in) (string) The module name to remove from the index.

#### Returns:
(bool) TRUE if the module was removed. FALSE if it was not present in the index.

---
### add_defaults()
#### Arguments:
__self__: (in) ([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md)) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object.

__defaults_: (in) ([Modulemd.Defaults](Modulemd.Defaults.md)) A [Modulemd.Defaults](Modulemd.Defaults.md) object to associate with this ([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md)).

#### Returns:
(void)

---
### get_defaults()
#### Arguments:
__self__: (in) ([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md)) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object.

__module_name__: (in) (string) The name of the module whose defaults should be returned.

__intent__: (in) (string) (nullable) Get the defaults for a particular intent. If this intent does not exist, this function will return the general defaults instead.

#### Returns:
([Modulemd.Defaults](Modulemd.Defaults.md)) (transfer none) The defaults of this module associated with this intent, the general defaults if the intent does not exist or NULL if neither exists.

---
### add_translation()
Adds a [Modulemd.Translation](Modulemd.Translation.md) to all of the appropriate module streams within this index. It will be checked for validity as part of this action and may return an error. It will also fail if the module and stream are not present in the index.

Note: once a [Modulemd.Translation](Modulemd.Translation.md) is added, it cannot be removed. It can be replaced with a subsequent call to this function with an object of the same module name and stream.

#### Arguments:
__self__: (in) ([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md)) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object.

__translation__: (in) ([Modulemd.Translation](Modulemd.Translation.md)) A translation object to add to the Index.

__error__: (out) (GError) If the validation failed, this will contain the reason.

#### Returns:
(bool) TRUE if the translation could be added. FALSE if it failed validation or the module stream it references does not appear in the index.

---
### upgrade()
#### Arguments
__self__: (in) ([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md)) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object.

__stream_version__: (in) (uint64) (nullable) Upgrade all [Modulemd.ModuleStream](Modulemd.ModuleStream.md) objects in this index to the specified version. If the version is unspecified (0 in the C API), it will be upgraded to the highest-supported version available.

__defaults_version__: (in) (uint64) (nullable) Upgrade all [Modulemd.Defaults](Modulemd.Defaults.md) objects in this index to the specified version. If the version is unspecified (0 in the C API), it will be upgraded to the highest-supported version available.

__error__: (out) (GError) If this function fails, reason why the upgrade could not be completed will be returned here.

#### Returns:
(bool) TRUE if all objects could be upgraded properly. FALSE if one or more failed. If FALSE is returned, the internal state of this [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) is undefined and it should be freed. In that situation, `error` will be set with more information about why it failed.

## Future enhancements
* Implement GInitable and add `new_from_file()` and friends.

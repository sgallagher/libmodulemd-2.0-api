# Modulemd.ModuleIndex(GObject)
A simplistic wrapper around GHashTable to ensure type-safety for [Modulemd.Module](Modulemd.Module.md) objects.

Implements:
* [Modulemd.YamlOutputIface](interfaces/Modulemd.YamlOutputIface.md)

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

## Public Virtual Methods

## Private Virtual Methods


## Future enhancements
* Implement GInitable and add `new_from_file()` and friends.

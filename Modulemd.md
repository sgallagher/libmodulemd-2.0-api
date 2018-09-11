# Modulemd
Utility functions not bound to any object. Used when parsing or emitting a complete data set.

## Properties
## Functions

---
### get_version()
#### Arguments:
#### Returns:
(string) The version of libmodulemd.

---
### index_from_file()
#### Arguments:
__yaml_file__: (in) (string) A YAML file containing the module metadata and other related information such as default streams.

__failures__: (out) (list<[Modulemd.Subdocument](Modulemd.Subdocument.md)>) An array containing any subdocuments from the YAML file that failed to parse. See [Modulemd.Subdocument](Modulemd.Subdocument.md) for more details.

__error__: (out) (GError) A GError containing additional information if this function completely fails.

#### Returns:
([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) An object containing all [Modulemd.Module](Modulemd.Module.md) objects (including defaults and translations) included in this YAML stream, indexed by the module name.

---
### index_from_string()
#### Arguments:
__yaml_string__: (in) (string) A YAML string containing the module metadata and other related information such as default streams.

__failures__: (out) (list<[Modulemd.Subdocument](Modulemd.Subdocument.md)>) An array containing any subdocuments from the YAML file that failed to parse. See [Modulemd.Subdocument](Modulemd.Subdocument.md) for more details.

__error__: (out) (GError) A GError containing additional information if this function completely fails.

#### Returns:
([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) An object containing all [Modulemd.Module](Modulemd.Module.md) objects (including defaults and translations) included in this YAML stream, indexed by the module name.

---
### index_from_stream()
#### Arguments:
__yaml_stream__: (in) (string) 	
A YAML stream containing the module metadata and other related information such as default streams.

__failures__: (out) (list<[Modulemd.Subdocument](Modulemd.Subdocument.md)>) An array containing any subdocuments from the YAML file that failed to parse. See [Modulemd.Subdocument](Modulemd.Subdocument.md) for more details.

__error__: (out) (GError) A GError containing additional information if this function completely fails.

#### Returns:
([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) An object containing all [Modulemd.Module](Modulemd.Module.md) objects (including defaults and translations) included in this YAML stream, indexed by the module name.

---
### dump_index()
#### Arguments:
__index__: (in) ([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md)) The index of [Modulemd.Module](Modulemd.Module.md) objects to dump to a YAML file.

__yaml_file__: (in) (string) The path to the file that should contain the resulting YAML.

__error__: (out) (GError) A GError containing the reason the function failed, NULL if the function succeeded.

#### Returns:
(bool) TRUE if the file was written successfully. In the event of an error, sets `error` appropriately and returns FALSE.

---
### dumps_index()
#### Arguments:
__index__: (in) ([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md)) The index of [Modulemd.Module](Modulemd.Module.md) objects to dump to a YAML string.

__error__: (out) (GError) A GError containing the reason the function failed, NULL if the function succeeded.

#### Returns:
(string) A YAML representation of the index as a string. In the event of an error, sets `error` appropriately and returns NULL.

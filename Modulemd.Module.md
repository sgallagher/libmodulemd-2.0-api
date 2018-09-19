# Modulemd.Module (GObject)

Collects all information about a module: all of its streams, defaults, etc.

## Properties

__module_name__: (ro) (string) The name of this module. Cannot be modified after construction.

## Public Methods

---
### new()

#### Arguments:
__module_name__: (in) (string) The name of the module.

#### Returns:
([Modulemd.Module](Modulemd.Module.md)) (transfer full) A newly allocated [Modulemd.Module](Modulemd.Module.md).

---
### copy()
#### Arguments:
__self__: (in) ([Modulemd.Module](Modulemd.Module.md)) This [Modulemd.Module](Modulemd.Module.md) object.

#### Returns:
([Modulemd.Module](Modulemd.Module.md)) (transfer full) A shallow copy of this [Modulemd.Module](Modulemd.Module.md) object.

---
### validate()
#### Arguments:
__self__: (in) ([Modulemd.Module](Modulemd.Module.md)) This [Modulemd.Module](Modulemd.Module.md) object.

__error__: (out) (GError) A GError containing the reason the object failed validation. NULL if the validation passed.

#### Returns
(bool) TRUE if validation passed.

---
### get_all_streams_as_list()
#### Arguments:
__self__: (in) ([Modulemd.Module](Modulemd.Module.md)) This [Modulemd.Module](Modulemd.Module.md) object.

####
(GPtrArray<[Modulemd.ModuleStream](Modulemd.ModuleStream.md)>) (transfer container) A list of all available stream objects associated with this module. There may be multiple streams with the same name and different version and context. The order of items in this list is not guaranteed.

---
### get_streams_by_stream_name_as_list()
#### Arguments:
__self__: (in) ([Modulemd.Module](Modulemd.Module.md)) This [Modulemd.Module](Modulemd.Module.md) object.

__stream__: (in) (string) The name of the stream to retrieve.

#### Returns:
(GPtrArray<[Modulemd.ModuleStream](Modulemd.ModuleStream.md)>) (transfer container) A list of all available stream objects associated with a particular stream name, sorted highest to lowest by the version. The same version may have more than one associated context.

---
### get_stream_by_NSVC()
#### Arguments:
__self__: (in) ([Modulemd.Module](Modulemd.Module.md)) This [Modulemd.Module](Modulemd.Module.md) object.

__stream__: (in) (string) The name of the stream to retrieve.

__version__: (in) (uint64) The version of the string to return.

__context__: (in) (string) The module context to identify the right stream.

#### Returns:
([Modulemd.ModuleStream](Modulemd.ModuleStream.md)) (transfer none) The requested stream object or NULL if no match was found.

---
### add_defaults()
#### Arguments:
__self__: (in) ([Modulemd.Module](Modulemd.Module.md)) This [Modulemd.Module](Modulemd.Module.md) object.

__defaults_: (in) ([Modulemd.Defaults](Modulemd.Defaults.md)) A [Modulemd.Defaults](Modulemd.Defaults.md) object to associate with this ([Modulemd.Module](Modulemd.Module.md). If the module_name in the [Modulemd.Defaults](Modulemd.Defaults.md) object does not match this module, it will be silently ignored.

#### Returns:
(void)

---
### get_defaults()
#### Arguments:
__self__: (in) ([Modulemd.Module](Modulemd.Module.md)) This [Modulemd.Module](Modulemd.Module.md) object.

__intent__: (in) (string) (nullable) Get the defaults for a particular intent. If this intent does not exist, this function will return the general defaults instead.

#### Returns:
([Modulemd.Defaults](Modulemd.Defaults.md)) (transfer none) The defaults of this module associated with this intent, the general defaults if the intent does not exist or NULL if neither exists.

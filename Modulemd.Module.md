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
### get_stream_names_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.Module](Modulemd.Module.md)) This [Modulemd.Module](Modulemd.Module.md) object.

#### Returns:
(strv) (transfer full) An ordered list of unique stream names associated with this module.

---
### get_stream()
#### Arguments:
__self__: (in) ([Modulemd.Module](Modulemd.Module.md)) This [Modulemd.Module](Modulemd.Module.md) object.

__stream_name__: (in) (string) The name of the stream to retrieve.

#### Returns:
([Modulemd.ModuleStream](Modulemd.ModuleStream.md)) (transfer none) The stream of the specified name, or NULL if the stream is not present in the index.

---
### add_defaults()
#### Arguments:
__self__: (in) ([Modulemd.Module](Modulemd.Module.md)) This [Modulemd.Module](Modulemd.Module.md) object.

__defaults_: (in) ([Modulemd.Defaults](Modulemd.Defaults.md)) A [Modulemd.Defaults](Modulemd.Defaults.md) object to associate with this ([Modulemd.Module](Modulemd.module.md). If the module_name in the [Modulemd.Defaults](Modulemd.Defaults.md) object does not match this module, it will be silently ignored.

#### Returns:
(void)

---
### get_defaults()
#### Arguments:
__self__: (in) ([Modulemd.Module](Modulemd.Module.md)) This [Modulemd.Module](Modulemd.Module.md) object.

__intent__: (in) (string) (nullable) Get the defaults for a particular intent. If this intent does not exist, this function will return the general defaults instead.

#### Returns:
([Modulemd.Defaults](Modulemd.Defaults.md)) (transfer none) The defaults of this module associated with this intent, the general defaults if the intent does not exist or NULL if neither exists.

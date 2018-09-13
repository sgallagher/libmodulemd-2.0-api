# Modulemd.Defaults (GObject)
Base class for modulemd-defaults objects.

Derived Objects:
* [Modulemd.DefaultsV1](Modulemd.DefaultsV1.md)

## Properties

__version__: (ro) The metadata version of this Defaults object. Defaults to the highest-supported version if not specified at object construction. Cannot be changed after object construction.

__module_name__: (ro) The name of the module to which these defaults apply.

## Public Methods

---
### new()
Create a new Defaults object of the type associated with the provided numeric version. If this function is not used and the version is not specified to `g_object_new`, object construction default to the highest-supported version.

#### Arguments:
__version__: (in) (uint64) The version of the Defaults metadata.

__module_name__: (in) (string) The name of the module to which these defaults apply.

#### Returns:
([Modulemd.Defaults](Modulemd.Defaults.md)) (transfer full) A newly-allocated Modulemd.Defaults object of the specified version.

---
### copy()
#### Arguments:
__self__: (in) ([Modulemd.Defaults](Modulemd.Defaults.md)) This [Modulemd.Defaults](Modulemd.Defaults.md) object.

#### Returns:
([Modulemd.Defaults](Modulemd.Defaults.md)) (transfer full) A shallow copy of this [Modulemd.Defaults](Modulemd.Defaults.md) object.

---
### validate()
#### Arguments:
__self__: (in) ([Modulemd.Defaults](Modulemd.Defaults.md)) This [Modulemd.Defaults](Modulemd.Defaults.md) object.

__error__: (out) (GError) A GError containing the reason the object failed validation, NULL if the validation passed.

#### Returns:
(bool) TRUE if validation passed.

---
### get_version()
Gets the numeric version associated with this object. This will never be modified after object construction.

#### Arguments:
__self__: (in) ([Modulemd.Defaults](Modulemd.Defaults.md)) This [Modulemd.Defaults](Modulemd.Defaults.md) object.

#### Returns:
(uint64) The metadata version represented by this [Modulemd.Defaults](Modulemd.Defaults.md) object.

---
### set_module_name()
Sets the module name. This should normally be done during object creation and remain unchanged. This object will fail validation if `module_name` is unset.

#### Arguments:
__self__: (in) ([Modulemd.Defaults](Modulemd.Defaults.md)) This [Modulemd.Defaults](Modulemd.Defaults.md) object.

__module_name__: (in) (string) The name of the module to which these defaults apply.

#### Returns:
(void)

---
### get_module_name()
#### Arguments:
__self__: (in) ([Modulemd.Defaults](Modulemd.Defaults.md)) This [Modulemd.Defaults](Modulemd.Defaults.md) object.

#### Returns:
(string) (transfer none) The name of the module to which these defaults apply.

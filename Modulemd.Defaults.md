# Modulemd.Defaults (GObject)
Base class for modulemd-defaults objects.

Derived Objects:
* [Modulemd.DefaultsV1](Modulemd.DefaultsV1.md)

## Properties

__version__: (ro) The metadata version of this Defaults object.

__module_name__: (ro) The name of the module to which these defaults apply.

## Public Methods

---
### new()
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

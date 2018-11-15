# Modulemd.Defaults (GObject)
A parent class for all versions of Defaults objects.

## Properties

__mdversion__: (ro) (uint64) The metadata version of this Defaults object. Defaults to the highest-supported version if not specified at object construction. Cannot be changed after object construction except through the upgrade() routine.

__module_name__: (ro) (string) The name of the module to which these defaults apply. Cannot be changed after object construction

## Public Methods

### new()

#### Arguments:
__version__: (in) (uint64) (nullable) The version of the Defaults metadata. If set to zero, uses the highest-available version.

__module_name__: (in) (string) The name of the module to which these defaults apply.

#### Returns:
([Modulemd.Defaults](Modulemd.Defaults.md)) (transfer full) A newly-allocated Modulemd.Defaults object of the subtype matching the provided version.

---
### copy()
#### Arguments:
__self__: (in) ([Modulemd.Defaults](Modulemd.Defaults.md)) This [Modulemd.Defaults](Modulemd.Defaults.md) object

#### Returns:
([Modulemd.Defaults](Modulemd.Defaults.md)) (transfer full) A shallow copy of this [Modulemd.Defaults](Modulemd.Defaults.md) object.

---
### upgrade()
Return an upgraded copy of this object. Does not modify the original.

#### Arguments:
__self__: (in) ([Modulemd.Defaults](Modulemd.Defaults.md)) This [Modulemd.Defaults](Modulemd.Defaults.md) object

__version__: (in) (uint64) (nullable) The version to upgrade to. If unspecified (0 in the C API), this will upgrade the defaults to the highest version supported.

__error__: (out) (GError) If this function fails, this argument will contain the reason why.

#### Returns:
([Modulemd.Defaults](Modulemd.Defaults.md)) (transfer full) Returns a newly-allocated [Modulemd.Defaults](Modulemd.Defaults.md) copy of this object upgraded to the requested version. Returns NULL and sets `error` appropriately if the upgrade could not be completed automatically.

---
### validate()
#### Arguments:
__self__: (in) ([Modulemd.Defaults](Modulemd.Defaults.md)) This [Modulemd.Defaults](Modulemd.Defaults.md) object.

__error__: (out) (GError) A GError containing the reason the object failed validation, NULL if the validation passed.

#### Returns:
(bool) TRUE if validation passed.

# Modulemd.Defaults (GObject)
A parent class for all versions of Defaults objects.

## Properties

## Public Methods
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

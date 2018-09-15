# Modulemd.ModuleStream (GObject)
A parent class for all versions of ModuleStream objects.

## Properties

## Public Methods

---
### copy()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStream](Modulemd.ModuleStream.md)) This [Modulemd.ModuleStream](Modulemd.ModuleStream.md) object.

#### Returns:
([Modulemd.ModuleStream](Modulemd.ModuleStream.md)) (transfer full) A shallow copy of this [Modulemd.ModuleStream](Modulemd.ModuleStream.md) object.

---
### upgrade()
Return an upgraded copy of this object. Does not modify the original.

#### Arguments:
__self__: (in) ([Modulemd.ModuleStream](Modulemd.ModuleStream.md)) This [Modulemd.ModuleStream](Modulemd.ModuleStream.md) object.

__version__: (in) (uint64) The version to upgrade to. If unspecified (0 in the C API), this will upgrade the stream to the highest version supported.

__error__: (out) (GError) If this function fails, this argument will contain the reason why.

#### Returns:
([Modulemd.ModuleStream](Modulemd.ModuleStream.md)) (transfer full). Returns a newly-allocated [Modulemd.ModuleStream](Modulemd.ModuleStream.md) copy of this object upgraded to the requested version. Returns NULL and sets `error` appropriately if the upgrade could not be completed automatically.

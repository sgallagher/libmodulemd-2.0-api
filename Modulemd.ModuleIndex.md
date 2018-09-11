# Modulemd.ModuleIndex(GObject)
A simplistic wrapper around GHashTable to ensure type-safety for [Modulemd.Module](Modulemd.Module.md) objects.

## Properties
__keys__: (ro) (GStrv) An ordered list of string keys in this index.

## Public Methods

---
### list_keys()
#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

#### Returns:
(GStrv) An ordered list of string keys in this index.

---
### get()
#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

__module_name__: (in) (string) The module name to look up in the index.

#### Returns:
The ([Modulemd.Module](Modulemd.Module.md)) object matching the provided key or NULL if the key was not present in the index.

---
---
### set()
#### Arguments:
__self__: (in) This [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object

__module__: (in) The [Modulemd.Module](Modulemd.Module.md) object to add to the index.

__error__: (out) (GError) A GError containing the reason the [Modulemd.Module](Modulemd.Module.md) object could not be added or NULL if the function succeeded.

#### Returns:
(bool) TRUE if the [Modulemd.Module](Modulemd.Module.md) object was added successfully. On failure, returns FALSE and sets `error` appropriately.

## Public Virtual Methods

## Private Virtual Methods

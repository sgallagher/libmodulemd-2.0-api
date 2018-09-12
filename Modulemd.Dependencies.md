# Modulemd.Dependencies(GObject)

## Interfaces:
Implements:
* [Modulemd.YamlIface](interfaces/Modulemd.YamlIface.md)

## Properties

---
__buildtime_modules__: (ro) (GStrv) The list of modules required at build-time.

__runtime_modules__: (ro) (GStrv) The list of modules required at run-time.

## Public Methods

---
### new()
#### Arguments:
#### Returns:
([Modulemd.Dependencies](Modulemd.Dependencies.md)) A newly-allocated [Modulemd.Dependencies](Modulemd.Dependencies.md) object.

---
### copy()
#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object

#### Returns:
([Modulemd.Dependencies](Modulemd.Dependencies.md)) A newly-allocated shallow copy of `self`.

---
### update()
Populate the contents of `self` with those from `src` without allocating a new object. All internal structures of `self` will be replaced with a shallow copy from `src`.

#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object

__src__: (in) A previously-allocated [Modulemd.Dependencies](Modulemd.Dependencies.md) object to copy data from.

#### Returns:
(void)

---
### add_buildtime_stream()
Add a single stream of a module that is required to build another dependent module. The matrix of streams and module names will be calculated by the build-system. If the provided module name is already present, the streams will be added (with deduplication).

#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object.

__module_name__: (in) (string) The name of the module to depend on.

__module_stream__: (in) (string) The name of the module stream to depend on.

#### Returns:
(void)

---
### get_buildtime_modules()
#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object.

#### Returns:
(GStrv) An ordered list of module names of build-time dependencies.

---
### get_buildtime_streams()
#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object.

__module__: (in) (string) The name of the module.

#### Returns:
(GStrv) An ordered list of module streams associated with the specified `module` that are required at build-time.

---
### add_runtime_stream()
Adds a module and its stream that is required at runtime by a dependent module. The matrix of streams and module names will be calculated by the build-system. If the listed provided module name is already present, the streams will be added (with deduplication).

#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object.

__module_name__: (in) (string) The name of the module to depend on.

__module_stream__: (in) (string) The name of the module stream to depend on.

#### Returns:
(void)

---
### get_runtime_modules()
#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object.

#### Returns:
(GStrv) An ordered list of module names of run-time dependencies.

---
### get_runtime_streams()
#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object.

__module__: (in) (string) The name of the module.

#### Returns:
(GStrv) An ordered list of module streams associated with the specified `module` that are required at run-time.

# Problems
* With this approach, the get_*() routines will need to be `(transfer full)` because they will be constructed from internal opaque structures. This conflicts with the convention of get() being `(transfer none)`

# Possible Alternatives
* Change name from get_\*() to something else. fetch_\*() perhaps?
* Consider replacing get_runtime_modules() and get_runtime_streams() with a Modulemd.DependenciesRuntimeIter approach. (Ditto buildtime)

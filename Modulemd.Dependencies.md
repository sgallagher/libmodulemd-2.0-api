# Modulemd.Dependencies(GObject)
Object to represent build-time and runtime dependencies of a module stream.

## Properties

## Public Methods

---
### new()
#### Arguments:
#### Returns:
([Modulemd.Dependencies](Modulemd.Dependencies.md)) (transfer full) A newly-allocated [Modulemd.Dependencies](Modulemd.Dependencies.md) object.

---
### copy()
#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object

#### Returns:
([Modulemd.Dependencies](Modulemd.Dependencies.md)) (transfer full) A newly-allocated shallow copy of `self`.

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
### get_buildtime_modules_as_strv()
#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object.

#### Returns:
(GStrv) (transfer full) An ordered list of module names of build-time dependencies.

---
### get_buildtime_streams_as_strv()
#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object.

__module__: (in) (string) The name of the module.

#### Returns:
(GStrv) (transfer full) An ordered list of module streams associated with the specified `module` that are required at build-time.

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
### get_runtime_modules_as_strv()
#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object.

#### Returns:
(GStrv) An ordered list of module names of run-time dependencies.

---
### get_runtime_streams_as_strv()
#### Arguments:
__self__: (in) This [Modulemd.Dependencies](Modulemd.Dependencies.md) object.

__module__: (in) (string) The name of the module.

#### Returns:
(GStrv) (transfer full) An ordered list of module streams associated with the specified `module` that are required at run-time.

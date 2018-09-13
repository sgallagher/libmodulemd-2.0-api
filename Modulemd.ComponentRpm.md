# Modulemd.ComponentRpm ([Modulemd.ComponentBase](Modulemd.ComponentBase.md))
An RPM component that goes into a module stream.

## Properties
__cache__: (rw) (string) The lookaside cache URL.

__ref__: (rw) (string) The commit ID in the SCM repository.

__repository__: (rw) (string) The URI of the SCM repository.

## Public Methods

---
### new()
#### Arguments:
#### Returns:
([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) A newly-allocated [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md).

---
### add_restricted_arch()
Restrict the list of architectures on which this RPM will be available. It may be called any number of times to indicate support on additional architectures. Use `reset_arches()` to return to "all architectures".
#### Arguments:
__self__: (in) ([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) This [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md) object.

__arch__: (in) (string) An architecture on which this package should be available.

#### Returns:
(void)

---
### reset_arches()
Indicate that this RPM component is available on all arches.

#### Arguments:
__self__: (in) ([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) This [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md) object.

#### Returns:
(void)

---
### get_arches_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) This [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md) object.

#### Returns:
(GStrv) (transfer full): A list of architectures on which this RPM should be available.

---
### add_multilib_arch()
Add an architectures on which this RPM will be multilib. It may be called any number of times. Use `reset_multilib_arches()` to return to "no architectures".
#### Arguments:
__self__: (in) ([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) This [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md) object.

__arch__: (in) (string) An architecture on which this package should be multilib.

#### Returns:
(void)

---
### reset_multilib_arches()
Indicate that this RPM component is multilib on no architectures.

#### Arguments:
__self__: (in) ([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) This [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md) object.

#### Returns:
(void)

---
### get_multilib_arches_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) This [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md) object.

#### Returns:
(GStrv) (transfer full): A list of architectures on which multilib should be available.

---
### set_cache()
#### Arguments:
__self__: ([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) This [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md) object.

__cache__: (in) (string) The lookaside cache URL.

#### Returns:
(void)

---
### get_cache()
#### Arguments:
__self__: ([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) This [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md) object.

#### Returns:
(string) (transfer none) The lookaside cache URL.

---
### set_ref()
#### Arguments:
__self__: ([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) This [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md) object.

__ref__: (in) (string) The commit ID in the SCM repository.

#### Returns:
(void)

---
### get_ref()
#### Arguments:
__self__: ([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) This [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md) object.

#### Returns:
(string) (transfer none) The commit ID in the SCM repository.


---
### set_repository()
#### Arguments:
__self__: ([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) This [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md) object.

__repository__: (in) (string) The URI of the SCM repository.

#### Returns:
(void)

---
### get_repository()
#### Arguments:
__self__: ([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) This [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md) object.

#### Returns:
(string) (transfer none) The URI of the SCM repository.

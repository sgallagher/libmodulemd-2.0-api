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

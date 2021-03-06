# Modulemd.ComponentModule ([Modulemd.Component](Modulemd.Component.md))
A module component that goes into a module stream.

## Properties
__ref__: (rw) (string) The commit ID in the SCM repository.

__repository__: (rw) (string) The URI of the SCM repository.

## Public Methods

---
### new()
#### Arguments:
#### Returns:
([Modulemd.ComponentModule](Modulemd.ComponentModule.md)) A newly-allocated [Modulemd.ComponentModule](Modulemd.ComponentModule.md).

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

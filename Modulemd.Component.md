# Modulemd.Component (GObject)
Pure virtual parent class for components that go into a module stream.

Derived Objects:
* [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)
* [Modulemd.ComponentModule](Modulemd.ComponentModule.md)
 
## Properties

__buildorder__: (rw) (int64) The order this component should be built relative to others.

__name__: (rw) (string) The name of the component.

__rationale__: (rw) (string) A description of the reason this component is part of the module stream.

## Public Methods

---
### copy()
#### Arguments:
__self__: (in) This [Modulemd.Component](Modulemd.Component.md) object.

#### Returns:
([Modulemd.Component](Modulemd.Component.md)) (transfer full) A shallow copy of this component.

---
### update()
Updates this component to be a shallow copy of `src`.

#### Arguments:
__self__: (in) This [Modulemd.Component](Modulemd.Component.md) object.

__src__: (in) ([Modulemd.Component](Modulemd.Component.md)) The object to copy from.

#### Returns:
(void)

---
### set_buildorder()
#### Arguments:
__self__: (in) This [Modulemd.Component](Modulemd.Component.md) object.

__buildorder__: (in) (int64) The order this component should be built relative to others.

#### Returns:
(void)

---
### get_buildorder()
#### Arguments:
__self__: (in) This [Modulemd.Component](Modulemd.Component.md) object.

#### Returns:
(int64) The value of the buildorder

---
### set_name()
#### Arguments:
__self__: (in) This [Modulemd.Component](Modulemd.Component.md) object.

__name__: (in) (string) The name of the component.

#### Returns:
(void)

---
### get_name()
#### Arguments:
__self__: (in) This [Modulemd.Component](Modulemd.Component.md) object.

#### Returns:
(string) (transfer none) The name of the component.

---
### set_rationale()
#### Arguments:
__self__: (in) This [Modulemd.Component](Modulemd.Component.md) object.

__rationale__: (in) (string) The reason that this component is part of the stream.

#### Returns:
(void)

---
### get_rationale()
__self__: (in) This [Modulemd.Component](Modulemd.Component.md) object.

#### Returns:
(string) (transfer none) The rationale.
Viewport
Window
×
×
×

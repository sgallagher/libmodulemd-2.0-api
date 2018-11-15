# Modulemd.ServiceLevel (GObject)

## Properties

__name__: (ro) (string) The name of this servicelevel. Must be set at object construction and may not be changed.

__eol__: (rw) (GDate) (nullable) The end-of-life date associated with this servicelevel

## Public Methods

---
### new()
#### Arguments:
__name__: (in) (string) The name of this servicelevel.

#### Returns:
([Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)) (transfer full) A newly-allocated [Modulemd.ServiceLevel](Modulemd.ServiceLevel.md) object.

---
### copy()
#### Arguments:
__self__: (in) ([Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)) This [Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)

#### Returns:
([Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)) (transfer full) A shallow copy of this object.

---
### set_eol()
#### Arguments:
__self__: (in) ([Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)) This [Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)

__eol__: (in) (GDate) The date that this service level goes end-of-life.

#### Returns:
(void)

---
### set_eol_ymd()
#### Arguments:
__self__: (in) ([Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)) This [Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)

__year__: (in) (int) The year that this service goes end-of-life.

__month__: (in) (int) The month that this service goes end-of-life.

__day__: (in) (int) The day that this service goes end-of-life.

#### Returns:
(void)

---
### remove_eol()
Remove the EOL from this Service Level.

#### Arguments:
__self__: (in) ([Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)) This [Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)

#### Returns:
(void)

---
### get_eol()
#### Arguments:
__self__: (in) ([Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)) This [Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)

#### Returns:
(GDate) (transfer none) The date this service level goes end of life.

---
### get_eol_as_string()
#### Arguments:
__self__: (in) ([Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)) This [Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)

#### Returns:
(string) (transfer full) The date this service level goes end of life as a string of the form 'YYYY-MM-DD'

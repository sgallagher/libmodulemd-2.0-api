# Modulemd.Buildopts (GObject)
Provides hints to the build-system on how to build this module.

## Properties
__rpm_macros__: (rw) (string) A string containing RPM build macros in the form that they would appear in an RPM macros file on-disk.

## Public Methods

---
### new()
#### Arguments:
#### Returns:
([Modulemd.Buildopts](Modulemd.Buildopts.md)) (transfer full) A newly-allocated [Modulemd.Buildopts](Modulemd.Buildopts.md) object.

---
### copy()
#### Arguments:
__self__: (in) ([Modulemd.Buildopts](Modulemd.Buildopts.md)) This [Modulemd.Buildopts](Modulemd.Buildopts.md) object.

#### Returns:
([Modulemd.Buildopts](Modulemd.Buildopts.md)) (transfer full) A shallow copy of this [Modulemd.Buildopts](Modulemd.Buildopts.md) object.

---
### set_rpm_macros()
#### Arguments:
__self__: (in) ([Modulemd.Buildopts](Modulemd.Buildopts.md)) This [Modulemd.Buildopts](Modulemd.Buildopts.md) object.
19

__rpm_macros__: (in) (string) A string containing RPM build macros in the form that they would appear in an RPM macros file on-disk.

#### Returns:
(void)

---
### get_rpm_macros()
#### Arguments:
__self__: (in) ([Modulemd.Buildopts](Modulemd.Buildopts.md)) This [Modulemd.Buildopts](Modulemd.Buildopts.md) object.

#### Returns:
(string) (transfer none) A string containing RPM build macros in the form that they would appear in an RPM macros file on-disk.

---
### add_rpm_to_whitelist()
#### Arguments:
__self__: (in) ([Modulemd.Buildopts](Modulemd.Buildopts.md)) This [Modulemd.Buildopts](Modulemd.Buildopts.md) object.

__rpm__: (in) (string) An RPM name to add to the whitelist.
#### Returns:
(void)

---
### remove_rpm_from_whitelist()
#### Arguments:
__self__: (in) ([Modulemd.Buildopts](Modulemd.Buildopts.md)) This [Modulemd.Buildopts](Modulemd.Buildopts.md) object.

__rpm__: (in) (string) An RPM name to remove from the whitelist.

#### Returns:
(void)

---
### get_rpm_whitelist_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.Buildopts](Modulemd.Buildopts.md)) This [Modulemd.Buildopts](Modulemd.Buildopts.md) object.

#### Returns:
(strv) (transfer full) An ordered list of all RPMs in the whitelist.

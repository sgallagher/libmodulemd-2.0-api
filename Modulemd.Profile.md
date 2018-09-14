# Modulemd.Profile (GObject)

Stores profile information for a module stream.

## Properties

__name__: (ro) (string) The name of this profile. Must be set at object construction and remains immutable thereafter.

__description__: (rw) (string) The untranslated description of this profile.

## Public Methods

---
### new()
#### Arguments:
__name__: (in) (string) The name of this profile.

#### Returns:
([Modulemd.Profile](Modulemd.Profile.md)) A newly-allocated [Modulemd.Profile](Modulemd.Profile.md) object.

---
### copy()
#### Arguments:
__self__: (in) ([Modulemd.Profile](Modulemd.Profile.md)) This [Modulemd.Profile](Modulemd.Profile.md) object.

#### Returns:
([Modulemd.Profile](Modulemd.Profile.md)) A shallow copy of this profile.

---
### set_description()
#### Arguments:
__self__: (in) ([Modulemd.Profile](Modulemd.Profile.md)) This [Modulemd.Profile](Modulemd.Profile.md) object.

__description__: (in) (string) The description of this profile in the C.UTF-8 locale.

#### Returns:
(void)

---
### get_description()
#### Arguments:
__self__: (in) ([Modulemd.Profile](Modulemd.Profile.md)) This [Modulemd.Profile](Modulemd.Profile.md) object.

__locale__: (in) (string) (nullable) The locale specifying the translation to return. If unspecified, it defaults to C.UTF-8

#### Returns:
(string) (transfer none) The description of this profile translated into the language specified by the locale if it is available, otherwise it returns the C.UTF-8 original.

---
### add_rpm()
#### Arguments:
__self__: (in) ([Modulemd.Profile](Modulemd.Profile.md)) This [Modulemd.Profile](Modulemd.Profile.md) object.

__rpm__: (in) (string) The name of a binary RPM that should be installed when this profile is selected for installation.

#### Returns:
(void)

---
### remove_rpm()
#### Arguments:
__self__: (in) ([Modulemd.Profile](Modulemd.Profile.md)) This [Modulemd.Profile](Modulemd.Profile.md) object.

__rpm__: (in) (string): The name of a binary RPM to remove from this profile.

#### Returns:
(void)

---
### get_rpms_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.Profile](Modulemd.Profile.md)) This [Modulemd.Profile](Modulemd.Profile.md) object.

#### Returns:
(strv) (transfer full) An ordered list of binary RPMs that would be installed when this profile is selected for installation.

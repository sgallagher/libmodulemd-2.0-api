# Modulemd.TranslationEntry (GObject)

Contains the translated strings of a module stream for a specific locale.

## Properties
__locale__: (ro) (string) The locale for this translation entry. It must correspond to the format specified by [libc locale names](https://www.gnu.org/software/libc/manual/html_node/Locale-Names.html). This field may only be set on object construction and is immutable afterwards.

__summary__: (rw) (string) The summary of this module stream translated into the language specified by `locale`.

__description__: (rw) (string) The description of this module stream translated into the language specified by `locale`.

## Public Methods

---
### new()
#### Arguments:
__locale__: (in) (string) The locale for this translation entry. It must correspond to the format specified by [libc locale names](https://www.gnu.org/software/libc/manual/html_node/Locale-Names.html).

Returns:
([Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)) A newly-allocated [Modulemd.TranslationEntry](Modulemd.TranslationEntry.md) object.

---
### copy()
#### Arguments:
__self__: (in) ([Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)) This [Modulemd.TranslationEntry](Modulemd.TranslationEntry.md) object.

#### Returns:
([Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)) A shallow copy of this [Modulemd.TranslationEntry](Modulemd.TranslationEntry.md).

---
### set_summary()
#### Arguments:
__self__: (in) ([Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)) This [Modulemd.TranslationEntry](Modulemd.TranslationEntry.md) object.

__summary__: (in) (string) The summary of this module translated appropriately for this locale.

#### Returns:
(void)

---
### get_summary()
#### Arguments:
__self__: (in) ([Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)) This [Modulemd.TranslationEntry](Modulemd.TranslationEntry.md) object.

#### Returns:
(string) (transfer none) The summary of this module translated appropriately for this locale.


---
### set_description()
#### Arguments:
__self__: (in) ([Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)) This [Modulemd.TranslationEntry](Modulemd.TranslationEntry.md) object.

__description__: (in) (string) The description of this module translated appropriately for this locale.

#### Returns:
(void)

---
### get_description()
#### Arguments:
__self__: (in) ([Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)) This [Modulemd.TranslationEntry](Modulemd.TranslationEntry.md) object.

#### Returns:
(string) (transfer none) The description of this module translated appropriately for this locale.

---
### get_profiles_as_strv()
Get a list of profiles that have descriptions.

#### Arguments:
__self__: (in) ([Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)) This [Modulemd.TranslationEntry](Modulemd.TranslationEntry.md) object.

#### Returns:
(strv) (transfer full) An ordered list of profiles for which descriptions have been translated for this locale.

---
### set_profile_description()
#### Arguments:
__self__: (in) ([Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)) This [Modulemd.TranslationEntry](Modulemd.TranslationEntry.md) object.

__profile_name__: (in) (string) The name of the profile whose description is being translated.

__profile_description__: (in) (string) The description of this profile translated appropriately for this locale.

#### Returns:
(void)

---
### get_profile_description()
#### Arguments:
__self__: (in) ([Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)) This [Modulemd.TranslationEntry](Modulemd.TranslationEntry.md) object.

__profile_name__: (in) (string) The name of the profile whose description is being translated.

#### Returns:
(string) (transfer none) The description of this profile translated appropriately for this locale.

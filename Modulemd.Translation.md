# Modulemd.Translation (GObject)
Translation information for a module stream.

## Properties
__version__: (ro) (uint64) The metadata version of this [Modulemd.Translation](Modulemd.Translation.md). Must be set at object construction time and remains immutable thereafter.

__module_name__: (ro) (string) The name of the module to which these translations apply. Must be set at object construction time and remains immutable thereafter.

__module_stream__: (ro) (string) The name of the module stream to which these translations apply. Must be set at object construction time and remains immutable thereafter.

__modified__: (rw) (uint64) The last modified time represented as a 64-bit integer (such as 201807011200)

## Public Methods

---
### new()
#### Arguments:
__version__: (in) (uint64) The metadata version of this [Modulemd.Translation](Modulemd.Translation.md).

__module_name__: (in) (string) The name of the module to which these translations apply.

__module_stream__: (in) (string) The name of the module stream to which these translations apply.

__modified__: (in) (uint64) The last modified time represented as a 64-bit integer (such as 201807011200)

#### Returns:
([Modulemd.Translation](Modulemd.Translation.md)) A newly-allocated [Modulemd.Translation](Modulemd.Translation.md) object.

---
### copy()
#### Arguments:
__self__: (in) ([Modulemd.Translation](Modulemd.Translation.md)) This [Modulemd.Translation](Modulemd.Translation.md) object.

#### Returns:
([Modulemd.Translation](Modulemd.Translation.md)) (transfer full) A shallow copy of this [Modulemd.Translation](Modulemd.Translation.md) object.

---
### validate()
his method ensures that the translation is internally consistent for usage or dumping to YAML. It will be run implicitly prior to emitting YAML. This is not a complete linter, merely a sanity check that the values are not impossible.
#### Arguments:
__self__: (in) ([Modulemd.Translation](Modulemd.Translation.md)) This [Modulemd.Translation](Modulemd.Translation.md) object.

__error__: (out) (GError) If the object is not valid, it will return the reason.

#### Returns:
(bool) TRUE if validation passed.

---
### dump()
#### Arguments:
__self__: (in) ([Modulemd.Translation](Modulemd.Translation.md)) This [Modulemd.Translation](Modulemd.Translation.md) object.

__yaml_file__: (in) (string) Path to the output file to contain a YAML representation of this object.

__error__: (out) (GError) If the YAML could not be written to disk, contains the reason.

#### Returns:
(bool) Whether the YAML was written successfully.

---
### dumps()
#### Arguments:
__self__: (in) ([Modulemd.Translation](Modulemd.Translation.md)) This [Modulemd.Translation](Modulemd.Translation.md) object.

__error__: (out) (GError) If the YAML could not be written to disk, contains the reason.

#### Returns:
(string) (transfer_full) A YAML string representing this object.

---
### set_modified()
#### Arguments:
__self__: (in) ([Modulemd.Translation](Modulemd.Translation.md)) This [Modulemd.Translation](Modulemd.Translation.md) object.

__modified__: (in) (uint64) The last modified time represented as a 64-bit integer (such as 201807011200)

#### Returns:
(void)

---
### get_locales_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.Translation](Modulemd.Translation.md)) This [Modulemd.Translation](Modulemd.Translation.md) object.

#### Returns:
(strv) (transfer full) An ordered list of locales known to this [Modulemd.Translation](Modulemd.Translation.md).

---
### set_translation_entry()
#### Arguments:
__self__: (in) ([Modulemd.Translation](Modulemd.Translation.md)) This [Modulemd.Translation](Modulemd.Translation.md) object.

__translation_entry__: (in) ([Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)) A set of translations of this module stream for a particular locale.

#### Returns:
(void)

---
### get_translation_entry()
#### Arguments:
__self__: (in) ([Modulemd.Translation](Modulemd.Translation.md)) This [Modulemd.Translation](Modulemd.Translation.md) object.

__locale__: (in) (string) The locale of the translation to retrieve.

#### Returns:
([Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)) The translation entry for the requested locale, or NULL if the locale was unknown.

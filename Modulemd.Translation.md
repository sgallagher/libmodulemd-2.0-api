# Modulemd.Translation (GObject)
Translation information for a module stream

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

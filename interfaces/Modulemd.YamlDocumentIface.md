# Modulemd.YamlDocumentIface
Interface for objects that can be represented as complete YAML documents.

## Public Virtual Methods

---
### dump()
#### Arguments:
__self__: (in) This [Modulemd.DocumentBase](Modulemd.DocumentBase.md)

__yaml_file__: (in) (string) The path to the file that should contain the resulting YAML.

__error__: (out) (GError) A GError containing the reason the function failed, NULL if the function succeeded.

#### Returns:
(bool) TRUE if the file was written successfully. In the event of an error, sets `error` appropriately and returns FALSE.

---
### dumps()
#### Arguments:
__self__: (in) This [Modulemd.DocumentBase](Modulemd.DocumentBase.md)

__error__: (out) (GError) A GError containing the reason the function failed, NULL if the function succeeded.

#### Returns:
(string) A YAML representation of the index as a string. In the event of an error, sets `error` appropriately and returns NULL.

---
### validate()
This method ensures that the object is internally consistent for usage. It will be run implicitly prior to emitting YAML.

#### Arguments:
__self__: (in) This [Modulemd.DocumentBase](Modulemd.DocumentBase.md)

__error__: (out) (GError) A GError containing the reason the object failed validation, NULL if the validation passed.

#### Returns:
(bool) TRUE if validation passed.

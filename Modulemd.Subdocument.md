# Modulemd.Subdocument (GObject)

## Properties
__yaml__: (ro) (string) A string containing the YAML subdocument.

__gerror__: (ro) (GError) A GError containing an error code and message about why this subdocument failed parsing.

## Public Methods

---
### new()
#### Arguments:
#### Returns:
([Modulemd.Subdocument](Modulemd.Subdocument.md)) A newly-allocated [Modulemd.Subdocument](Modulemd.Subdocument.md) object.

---
### get_yaml()
#### Arguments:
__self__: (in) This [Modulemd.Subdocument](Modulemd.Subdocument.md)

#### Returns:
(string) The associated YAML subdocument

---

### get_gerror()
#### Arguments:
__self__: (in) This [Modulemd.Subdocument](Modulemd.Subdocument.md)

#### Returns:
(GError) A GError containing an error code and message about why this subdocument failed parsing.

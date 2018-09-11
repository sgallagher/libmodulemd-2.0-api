# Modulemd.YamlBase(GObject)
Base class for object types that can be represented as sections of a YAML document.

## Properties

## Public Methods

## Public Virtual Methods 

## Private Virtual Methods

---
### new_from_yaml()
#### Arguments:

__parser__: (in) (yaml_parser_t) A YAML parser object that has been positioned at the start of a YAML section representing this object type.

__error__: (out) (GError) A GError containing the reason the function failed, NULL if the function succeeded.

#### Returns:
([Modulemd.YamlBase](Modulemd.YamlBase.md)) Object constructed from YAML stream. In the event of a parsing or data error, sets `error` appropriately and returns NULL.

---
### emit_yaml()
#### Arguments:
__self__: (in) This [Modulemd.YamlBase](Modulemd.YamlBase.md)

__emitter__: (in) (yaml_emitter_t) A YAML emitter object that has been initialized to include at least STREAM_START and DOCUMENT_START.

__error__: (out) (GError) A GError containing the reason the function failed, NULL if the function succeeded.

#### Returns:
(bool) TRUE if YAML could be emitted successfully. In the event of an error, sets `error` appropriately and returns FALSE.

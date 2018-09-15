# Modulemd.ModuleStreamV2 ([Modulemd.ModuleStream](Modulemd.ModuleStream.md))
The data to represent a stream of a module as described by a modulemd YAML document of version 2.

## Properties

__arch__: (rw) (string) Module Artifact Architecture

__buildopts__: (rw) ([Modulemd.BuildOpts](Modulemd.BuildOpts.md)) Build options for the module.

__community__: (rw) (string) Link to the upstream community for this module.

__context__: (rw) (string) The module context. Used for module stream expansion.

__description__: (rw) (string) The untranslated description of this module.

__documentation__: (rw) (string) Link to the upstream documentation for this module.

__name__: (ro) (string) The name of the module to which this stream applies. Set at object construction and immutable thereafter.

__stream__: (ro) (string) The stream name. Set at object construction and immutable thereafter.

__summary__: (rw) (string) The untranslated summary of this module.

__tracker__: (rw) (string) Link to the upstream bug tracker for this module.

__version__: (rw) (uint64) The version of this module.

## Public Methods

---
### new()
#### Arguments:
__module_name__: (in) (string) The name of the module.

__module_stream__: (in) (string) The name of the stream of the module.

#### Returns:
([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) (transfer full) A newly-allocated [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

---
### copy()
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

#### Returns:
([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) (transfer full) A shallow copy of this [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

---
### set_arch()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

__arch__: (in) (string) The module artifact architecture.

#### Returns:
(void)

---
### get_arch()
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

#### Returns:
(string) (transfer none) The module artifact architecture.

---
### set_buildopts()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

__buildopts__: (in) ([Modulemd.Buildopts](Modulemd.Buildopts)) Build options for this module.

#### Returns:
(void)

---
### get_buildopts()
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

####:
([Modulemd.Buildopts](Modulemd.buildopts.md)) (transfer none) The build options for this module.

---
### set_community()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

__community__: (in) (string) Link to the upstream community.

#### Returns:
(void)

---
### get_community()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

#### Returns:
(string) (transfer none) Link to the upstream community.

---
### add_component()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

__component__: (in) ([Modulemd.ComponentBase](Modulemd.ComponentBase.md)) A component to be added to this module stream.
#### Returns:
(void)

---
### add_content_license()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

__license__: (in) (string) A license under which the components of this module stream are distributed.

#### Returns:
(void)

---
### remove_content_license()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

__license__: (in) (string) A license to remove from the list. Ignored if not present.

#### Returns:
(void)

---
### get_content_licenses_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

#### Returns:
(strv) (transfer full) An ordered list of content licenses applicable to this module stream.

---
### set_context()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

__context__: (in) (string) The context for this module stream.

#### Returns:
(void)

---
### get_context()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

#### Returns:
(string) (transfer none) The context for this module stream.

---
### add_dependencies()
Add a [Modulemd.Dependencies](Modulemd.Dependencies.md) object to the list of dependencies for this module stream.
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

__dependencies__: (in) ([Modulemd.Dependencies](Modulemd.Dependencies.md)) A dependencies object to add to the list for this module stream.

#### Returns:
(void)

---
### get_dependencies_as_list()
Return the list of dependencies objects as a GPtrArray.

#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

#### Returns:
(GPtrArray<[Modulemd.Dependencies](Modulemd.Dependencies)>) (transfer container) A list of all [Modulemd.Dependencies](Modulemd.Dependencies) objects associated with this module stream.

---
### set_description()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

__description__: (in) (string) The untranslated description of this module stream.

#### Returns:
(void)

---
### get_description()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

__locale__: (in) (string) (nullable) The locale specifying the translation to return. If unspecified, it defaults to C.UTF-8

#### Returns:
(string) (transfer none) The description of this module stream translated into the language specified by the locale if it is available, otherwise it returns the C.UTF-8 original.

---
### set_documentation()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

__documentation__: (in) (string) Link to upstream documentation of this module stream.

#### Returns:
(void)

---
### get_documentation()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

#### Returns:
(string) Link to upstream documentation of this module stream.

---
### get_module_component_names_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

#### Returns:
(strv) (transfer full) An ordered list of module component names included in this stream.

---
### get_module_component()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)) This [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md) object.

__component_name__: (in) (string) The name of the module component to retrieve.

#### Returns:
([Modulemd.ComponentModule](Modulemd.ComponentModule.md)) (transfer none) A component module matching the supplied name or NULL if it was not found in this module stream.

# TODO

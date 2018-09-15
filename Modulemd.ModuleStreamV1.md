# Modulemd.ModuleStreamV1 ([Modulemd.ModuleStream](Modulemd.ModuleStream.md))
The data to represent a stream of a module as described by a modulemd YAML document of version 1.

## Properties

__arch__: (rw) (string) Module Artifact Architecture

__buildopts__: (rw) ([Modulemd.BuildOpts](Modulemd.BuildOpts.md)) Build options for the module.

__community__: (rw) (string) Link to the upstream community for this module.

__context__: (rw) (string) The module context. Used for module stream expansion.

__description__: (rw) (string) The untranslated description of this module.

__documentation__: (rw) (string) Link to the upstream documentation for this module.

__eol__: (ro) (GDate) (obsolete) The end-of-life date of this module stream. Use servicelevels instead.

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
([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) (transfer full) A newly-allocated [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

---
### copy()
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) (transfer full) A shallow copy of this [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

# TODO

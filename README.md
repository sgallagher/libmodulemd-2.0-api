# libmodulemd-2.0-api

## Quick Usage
```
from gi.repository import Modulemd

module_idx = Modulemd.ModuleIndex()
module_idx.update_from_file("mmd_from_repository.yaml")

testmodule = module_idx.get_module("testmodule")
testmodulestream = testmodule.get_stream("stable")

dependencies = testmodulestream.get_dependencies_as_list()
```

## Public Classes
* [Modulemd.Buildopts](Modulemd.Buildopts.md)
* [Modulemd.ComponentBase](Modulemd.ComponentBase.md)
* [Modulemd.ComponentModule](Modulemd.ComponentModule.md)
* [Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)
* [Modulemd.Defaults](Modulemd.Defaults.md)
* [Modulemd.DefaultsV1](Modulemd.DefaultsV1.md)
* [Modulemd.Dependencies](Modulemd.Dependencies.md)
* [Modulemd.Module](Modulemd.Module.md)
* [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md)
* [Modulemd.ModuleStream](Modulemd.ModuleStream.md)
* [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)
* [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV2.md)
* [Modulemd.Prioritizer](Modulemd.Prioritizer.md)
* [Modulemd.Profile](Modulemd.Profile.md)
* [Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)
* [Modulemd.Subdocument](Modulemd.Subdocument.md)
* [Modulemd.Translation](Modulemd.Translation.md)
* [Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)
* [Modulemd](Modulemd.md)


# General themes
* Any routine of the form `get_<property>()` will return a const pointer to the internal representation of this property.
* Any routine of the form `get_<property>_as_<type>()` will return a newly-allocated representation of the data in the specified format.

# Glossary
## Shallow Copy
For the purposes of this API, a "shallow copy" is defined as "A copy that takes a reference on any attribute of the source that it can and makes a full copy if it cannot."

For example, if an object "ObjectA" has members that are a string and a pointer to Object B, it would make a full `strcpy()` of the string but take a reference to Object B instead.

## Deep Copy
For the purposes of this API, a "deep copy" is a recursive descent of the object, making deep copies of any child objects wihtin it.

# libmodulemd-2.0-api
WIP module design

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
* [Modulemd.ModuleStream](Modulemd.ModuleStream.md) TODO
* [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) TODO
* [Modulemd.ModuleStreamV2](Modulemd.ModuleStreamV1.md) TODO
* [Modulemd.Prioritizer](Modulemd.Prioritizer.md)
* [Modulemd.Profile](Modulemd.Profile.md)
* [Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)
* [Modulemd.Subdocument](Modulemd.Subdocument.md)
* [Modulemd](Modulemd.md)

## Private Classes
These classes are not public API. Do not use them. The are internal implementation details.
* [Modulemd.Translation](Modulemd.Translation.md)
* [Modulemd.TranslationEntry](Modulemd.TranslationEntry.md)

# Glossary
## Shallow Copy
For the purposes of this API, a "shallow copy" is defined as "A copy that takes a reference on any attribute of the source that it can and makes a full copy if it cannot."

For example, if an object "ObjectA" has members that are a string and a pointer to Object B, it would make a full `strcpy()` of the string but take a reference to Object B instead.

## Deep Copy
For the purposes of this API, a "deep copy" is a recursive descent of the object, making deep copies of any child objects wihtin it.

# Modulemd.Prioritizer (GObject)
Class to aid in merging module metadata from multiple repositories.

## Properties

## Public Methods

---
### new()
#### Arguments:

#### Returns:
([Modulemd.Prioritizer](Modulemd.Prioritizer.md)) (transfer full) A newly-allocated [Modulemd.Prioritizer](Modulemd.Prioritizer.md) object.

---
### add_index()
Merge in the contents of a [Modulemd.ModuleIndex])(Modulemd.ModuleIndex.md) at the specified priority level. If other objects already exist at this level, they will be merged at this time.

#### Arguments:
__self__: (in) ([Modulemd.Prioritizer](Modulemd.Prioritizer.md)) This [Modulemd.Prioritizer](Modulemd.Prioritizer.md) object.

__index__: (in) ([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md)) The index of module objects from a repository whose contents will be merged depending on priority.

__priority__: (in) (int64) The priority of the repository this index was loaded from. Items at the same priority level will attempt to merge on conflict. Items at higher priority levels will replace on conflict. Valid values are 0 - 1000.

__error__: (out) (GError) If a failure to merge at this priority level occurs, `error` will contain information about why.

#### Returns:
(bool) TRUE if the objects could be added without generating a conflict at this priority level. If a conflict was detected, this function returns FALSE and `error` is set appropriately. If this function returns FALSE, the internal state of this object is undefined.

---
### resolve()
Merges all added [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) objects according to their priority.

#### Arguments:
__self__: (in) ([Modulemd.Prioritizer](Modulemd.Prioritizer.md)) This [Modulemd.Prioritizer](Modulemd.Prioritizer.md) object.
21

__error__: (out) (GError) If a merge failure occurs, `error` will contain information about why.

#### Returns:
([Modulemd.ModuleIndex](Modulemd.ModuleIndex.md)) (transfer full) A newly-allocated [Modulemd.ModuleIndex](Modulemd.ModuleIndex.md) object containing all the merged values of those that have been added to this object. If the merge could not be resolved, this function returns NULL and will set `error` appropriately.

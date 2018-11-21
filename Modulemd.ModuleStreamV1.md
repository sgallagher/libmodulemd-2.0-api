# Modulemd.ModuleStreamV1 ([Modulemd.ModuleStream](Modulemd.ModuleStream.md))
The data to represent a stream of a module as described by a modulemd YAML document of version 1.

## Properties

__arch__: (rw) (string) Module Artifact Architecture

__buildopts__: (rw) ([Modulemd.BuildOpts](Modulemd.BuildOpts.md)) Build options for the module.

__community__: (rw) (string) Link to the upstream community for this module.

__context__: (rw) (string) The module context. Used for module stream expansion.

__description__: (rw) (string) The untranslated description of this module.

__documentation__: (rw) (string) Link to the upstream documentation for this module.

__summary__: (rw) (string) The untranslated summary of this module.

__tracker__: (rw) (string) Link to the upstream bug tracker for this module.

## Public Methods

---
### new()
#### Arguments:
__module_name__: (in) (string) The name of the module.

__module_stream__: (in) (string) The name of the stream of the module.

#### Returns:
([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) (transfer full) A newly-allocated [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

---
### set_arch()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__arch__: (in) (string) The module artifact architecture.

#### Returns:
(void)

---
### get_arch()
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(string) (transfer none) The module artifact architecture.

---
### add_buildtime_requirement()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__module_name__: (in) (string) The name of the module to depend on.

__module_stream__: (in) (string) The name of the module stream to depend on.

#### Returns:
(void)

---
### remove_buildtime_requirement()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__module_name__: (in) (string) The name of the module to remove from the build-time dependencies.

#### Returns:
(void)

---
### get_buildtime_modules_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(strv) (transfer full) An ordered list of module names to depend on.

---
### get_buildtime_requirement_stream ()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__module_name__: (in) (string) The name of the module

#### Returns:
(strv) (transfer none) The name of the stream matching this module name.

---
### set_buildopts()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__buildopts__: (in) ([Modulemd.Buildopts](Modulemd.Buildopts)) Build options for this module.

#### Returns:
(void)

---
### get_buildopts()
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

####:
([Modulemd.Buildopts](Modulemd.buildopts.md)) (transfer none) The build options for this module.

---
### set_community()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__community__: (in) (string) Link to the upstream community.

#### Returns:
(void)

---
### get_community()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(string) (transfer none) Link to the upstream community.

---
### add_component()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__component__: (in) ([Modulemd.ComponentBase](Modulemd.ComponentBase.md)) A component to be added to this module stream.
#### Returns:
(void)

---
### add_content_license()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__license__: (in) (string) A license under which the components of this module stream are distributed.

#### Returns:
(void)

---
### remove_content_license()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__license__: (in) (string) A license to remove from the list. Ignored if not present.

#### Returns:
(void)

---
### get_content_licenses_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(strv) (transfer full) An ordered list of content licenses applicable to this module stream.

---
### set_context()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__context__: (in) (string) The context for this module stream.

#### Returns:
(void)

---
### get_context()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(string) (transfer none) The context for this module stream.

---
### set_description()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__description__: (in) (string) The untranslated description of this module stream.

#### Returns:
(void)

---
### get_description()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__locale__: (in) (string) (nullable) The locale specifying the translation to return. If unspecified, it defaults to C.UTF-8

#### Returns:
(string) (transfer none) The description of this module stream translated into the language specified by the locale if it is available, otherwise it returns the C.UTF-8 original.

---
### set_documentation()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__documentation__: (in) (string) Link to upstream documentation of this module stream.

#### Returns:
(void)

---
### get_documentation()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(string) Link to upstream documentation of this module stream.

### remove_module_component()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__component_name__: (in) (string) The name of the module component to remove.

#### Returns:
(void)

---
### set_eol()
Comptibility function with early iterations of modulemd v1. This function is a wrapper for Modulemd.ModuleStreamV1.add_servicelevel("rawhide", eol).
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__eol__: (in) (GDate) The end-of-life date for the "rawhide" service level.

#### Returns:
(void)

---
### get_eol()
Compatibility function with early iterations of modulemd v1. This function is a wrapper for Modulemd.ModuleStreamV1.get_servicelevel("rawhide").
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(GDate) (transfer none) The end-of-life date for the "rawhide" service level.

---
### get_module_component_names_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(strv) (transfer full) An ordered list of module component names included in this stream.

---
### get_module_component()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__component_name__: (in) (string) The name of the module component to retrieve.

#### Returns:
([Modulemd.ComponentModule](Modulemd.ComponentModule.md)) (transfer none) A component module matching the supplied name or NULL if it was not found in this module stream.

---
### add_module_license()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__license__: (in) (string) A license under which this module stream is released.

#### Returns:
(void)

---
### remove_module_license()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__license__: (in) (string) A license to remove from the list. Has no effect if the license is not present.

#### Returns:
(void)

---
### get_module_licenses_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(strv) (transfer full) An ordered list of licenses under which this module stream is released.

---
### get_module_name()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(string) (transfer none) The name of the module to which this stream belongs.

---
### get_nsvc_as_string()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(string) (transfer full) 

---
### add_profile()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__profile__: (in) ([Modulemd.Profile](Modulemd.Profile.md)) A profile definition to add to this module.

#### Returns:
(void)

---
### clear_profiles()
Remove all profiles from this module.
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(void)

---
### get_profile_names_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(strv) (transfer full) An ordered list of profile names associated with this module stream.

---
### get_profile()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__profile_name__: (in) (string) The name of the profile to retrieve.

#### Returns:
([Modulemd.Profile](Modulemd.Profile.md)) (transfer none) The requested profile definition or NULL if not found.


---
### add_rpm_api()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__api__: (in) (string) The name of a binary RPM present in this module that is considered stable public API.

#### Returns:
(void)

---
### remove_rpm_api()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__api__: (in) (string) A binary RPM name to remove from the list of stable public API.

#### Returns:
(void)

---
### get_rpm_api_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(strv) (transfer full) An ordered list of binary RPM names that forms the public API of this module stream.

---
### add_rpm_artifact()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__artifact__: (in) (string) The name of a binary RPM present in this module stream.

#### Returns:
(void)

---
### remove_rpm_artifact()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__artifact__: (in) (string) A binary RPM name to remove from the list of artifacts.

#### Returns:
(void)

---
### get_rpm_artifacts_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(strv) (transfer full) An ordered list of binary RPM names that are included in this module stream.

---
### remove_rpm_component()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__component_name__: (in) (string) The name of the RPM component to remove.

#### Returns:
(void)

---
### get_rpm_component_names_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(strv) (transfer full) An ordered list of RPM component names included in this stream.

---
### get_rpm_component()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__component_name__: (in) (string) The name of the RPM component to retrieve.

#### Returns:
([Modulemd.ComponentRpm](Modulemd.ComponentRpm.md)) (transfer none) An RPM module matching the supplied name or NULL if it was not found in this module stream.


---
### add_rpm_filter()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__rpm_name__: (in) (string) The name of a binary RPM to filter out of this module stream.

#### Returns:
(void)

---
### remove_rpm_filter()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__rpm_name__: (in) (string) A binary RPM name to remove from the filter list.

#### Returns:
(void)

---
### get_rpm_filters_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(strv) (transfer full) An ordered list of binary RPM names that are filtered out of this module stream.

---
### add_runtime_requirement()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__module_name__: (in) (string) The name of the module to depend on.

__module_stream__: (in) (string) The name of the module stream to depend on.

#### Returns:
(void)

---
### remove_runtime_requirement()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__module_name__: (in) (string) The name of the module to remove from the build-time dependencies.

#### Returns:
(void)

---
### get_runtime_modules_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(strv) (transfer full) An ordered list of module names to depend on.

---
### get_runtime_requirement_stream ()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__module_name__: (in) (string) The name of the module

#### Returns:
(strv) (transfer none) The name of the stream matching this module name.

---
### add_servicelevel()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__servicelevel__: (in) ([Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)) A service level to assign to this stream. If the name of this stream already exists, it will be replaced by this one.

#### Returns:
(void)

---
### remove_servicelevel()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__servicelevel_name__: (in) (string) The name of the service level to remove. If this name is not present, this function does nothing.

#### Returns:
(void)

---
### get_servicelevel_names_as_strv()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(strv) (transfer full) The ordered list of service level names associated with this module stream.

---
### get_servicelevel()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__servicelevel_name__: (in) (string) The name of the servicelevel to retrieve.

#### Returns:
([Modulemd.ServiceLevel](Modulemd.ServiceLevel.md)) (transfer none) The requested service level if it is present. NULL if unknown.

---
### set_summary()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__description__: (in) (string) The untranslated summary of this module stream.

#### Returns:
(void)

---
### get_summary()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__locale__: (in) (string) (nullable) The locale specifying the translation to return. If unspecified, it defaults to C.UTF-8

#### Returns:
(string) (transfer none) The summary of this module stream translated into the language specified by the locale if it is available, otherwise it returns the C.UTF-8 original.

---
### set_tracker()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__tracker__: (in) (string) Link to the upstream bug tracker.

#### Returns:
(void)

---
### get_tracker()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(string) (transfer none) Link to the upstream bug tracker.

---
### set_version()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__version__: (in) (uint64) The version of this module stream.

#### Returns:
(void)

---
### unset_version()
Remove the stream version from this module
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(void)

---
### get_version()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.
__version__: (out) (uint64) The version of this module stream

#### Returns:
(bool) Whether a version was set for this stream.

---
### set_xmd()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

__xmd__: (in) (GHashTable<string, GVariant>) An extensible metadata block consisting of arbitrary YAML data.

#### Returns:
(void)


---
### get_xmd_as_hash_table()
#### Arguments:
__self__: (in) ([Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md)) This [Modulemd.ModuleStreamV1](Modulemd.ModuleStreamV1.md) object.

#### Returns:
(GHashTable<string, GVariant>) (transfer container) The extensible metadata block represented as a hash table of <string, GVariant>

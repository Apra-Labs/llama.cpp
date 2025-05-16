# Changelog

## Changes since master branch

### Added
- Added common and llava as static libraries
  - Modified `CMakeLists.txt` to add new library targets
  - Added build configuration for static libraries
- Added logger header for improved logging functionality
  - Added new logging system in common library
- Added clip and llava headers for public use
  - Added public headers in `include/llama` directory
  - Configured installation paths for public headers
- Added common.h header as public header
  - Made common headers accessible through public API

### Changed
- Changed llava library name to llavalib for better clarity
  - Updated library target name in `CMakeLists.txt`
  - Modified all references to use new library name
- Resolved common name to common_llama to avoid naming conflicts
  - Renamed common library target in `common/CMakeLists.txt`
  - Updated all dependent targets to use new name
- Resolved llava header path for better organization
  - Reorganized header files in project structure
  - Updated include paths in build system
- Moved public headers of installation to include/llama to avoid conflict with whisper
  - Modified installation paths in `CMakeLists.txt`
  - Updated header search paths in build configuration

### Technical Details
- All changes are part of the vcpkg port implementation
- Changes focus on library organization and header management
- Improved build system configuration for better integration

### Modified Files
- `CMakeLists.txt`
  - Updated library targets and build configuration
  - Modified installation paths for headers
  - Added new static library configurations
  - Updated public header management
- `common/CMakeLists.txt`
  - Renamed common library target
  - Updated build dependencies
  - Modified header installation paths
  - Added new source files to build

### Build System Impact
- All changes maintain backward compatibility
- Improved organization of public headers
- Better separation of internal and public APIs
- Enhanced static library support
- Maintained CUDA support throughout changes 
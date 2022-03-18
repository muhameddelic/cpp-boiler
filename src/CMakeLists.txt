#-----------------------------------------------------------------

# The src directory contains all your modules.

#-----------------------------------------------------------------

# List of modules.
# Each directory can be its own module/target, its output being a binary:
#   - Executable
#   - Static & Shared libraries

set(_MODULES
  hello-lib
  hello-app
)

#-----------------------------------------------------------------

foreach(module ${_MODULES})
  add_subdirectory("${module}")
endforeach()

#-----------------------------------------------------------------

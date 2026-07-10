# This is template feel free to change stuff your liking.
# Comments are provided to let you understand what each command does.

# CMake configurations.
cmake_minimum_required(VERSION ${CMAKE_VERSION}) # This set the minimum CMake version needed. This line is not needed but it removes an annoying warning.

# Project configurations.
project(ENTER_PROJECT_NAME LANGUAGES C CXX) # Create a C/C++ CMake project with a given name.
file(GLOB_RECURSE SOURCES CONFIGURE_DEPENDS "${PROJECT_SOURCE_DIR}/src/*.c" "${PROJECT_SOURCE_DIR}/src/*.cpp") # Extract all the source files from the folder src/.
add_executable(${PROJECT_NAME} ${SOURCES}) # Attach all the source files to an executable with the name of the project.

# C/C++ configurations.
set(CMAKE_CXX_STANDARD 26) # Use C++26 standard.
set(CMAKE_CXX_STANDARD_REQUIRED OFF) # If C++26 standard is not supported go to the latest supported standard.
set(CMAKE_CXX_EXTENSIONS OFF) # Remove compiler specific extensions for portability.
target_include_directories(${PROJECT_NAME} PRIVATE ${PROJECT_SOURCE_DIR}/include) # Removed the need to do #include "include/example.h" which let you simply do #include "example.h".
target_compile_definitions(${PROJECT_NAME} PRIVATE PROJECT_ROOT="${PROJECT_SOURCE_DIR}") # Insert a macro like this - #define PROJECT_ROOT "**Absloute path to the project root**"
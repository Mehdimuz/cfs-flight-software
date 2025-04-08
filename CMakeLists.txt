cmake_minimum_required(VERSION 3.10)
project(cfs_flight_software C)

# Set output directory
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# Global flags
set(CMAKE_C_STANDARD 11)
add_definitions(-Wall)

# Include core and mission apps
add_subdirectory(core_apps)
add_subdirectory(mission_apps)

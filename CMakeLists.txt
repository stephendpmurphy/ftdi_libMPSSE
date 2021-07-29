# Set min req version of Cmake
cmake_minimum_required(VERSION 3.16)

# Set the project name
project(FTDI_MPSSE_Lib)

# Set our include directories
include_directories(src inc)

# Set our source files
set(LIB_SRC ${CMAKE_CURRENT_SOURCE_DIR}/src/ftdi_common.c
            ${CMAKE_CURRENT_SOURCE_DIR}/src/ftdi_i2c.c
            ${CMAKE_CURRENT_SOURCE_DIR}/src/ftdi_infra.c
            ${CMAKE_CURRENT_SOURCE_DIR}/src/ftdi_mid.c
            ${CMAKE_CURRENT_SOURCE_DIR}/src/ftdi_spi.c
)

# Set the lib output folderj
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ../lib)

# Create our static library
add_library(MPSSE STATIC ${LIB_SRC})
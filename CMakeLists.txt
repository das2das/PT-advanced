cmake_minimum_required(VERSION 3.10)

# set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake/Modules")
# message("Hi ${CMAKE_MODULE_PATH}")
# find_package(SFML REQUIRED system window graphics network audio)

include_directories(../sfml/include)
link_directories(../sfml/lib)

if(MSVC)
    set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} /NODEFAULTLIB:msvcrt")
endif()

add_subdirectory(src)

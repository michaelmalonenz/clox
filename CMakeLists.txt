cmake_minimum_required (VERSION 3.0)
project (comet)
enable_language(C)
enable_language(CXX)

if (WIN32)
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS}")
elseif (CMAKE_BUILD_TYPE MATCHES DEBUG)
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -O0 -g -ggdb3 -Wall -Wextra -Werror")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O0 -g -ggdb3 -Wall -Wextra -Werror")
endif ()

set(CMAKE_C_STANDARD 11 CACHE INTERNAL "Set C standard to C11")
set(CMAKE_CXX_STANDARD 20 CACHE INTERNAL "Set C++ standard to C++20")
set(CMAKE_LINKER_FLAGS "${CMAKE_LINKER_FLAGS}")

add_subdirectory(clox)

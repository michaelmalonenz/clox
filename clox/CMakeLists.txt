set(SOURCE
chunk.c
debug.c
main.c
memory.c
value.c
)


add_executable(clox "${SOURCE}")

target_include_directories(clox PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/inc")
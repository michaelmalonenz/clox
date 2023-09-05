set(SOURCE
chunk.c
compiler.c
debug.c
main.c
memory.c
scanner.c
value.c
vm.c
)


add_executable(clox "${SOURCE}")

target_include_directories(clox PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/inc")
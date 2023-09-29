set(SOURCE
chunk.c
compiler.c
debug.c
main.c
memory.c
object.c
scanner.c
table.c
value.c
vm.c
)

set (HEADERS
inc/chunk.h
inc/common.h
inc/compiler.h
inc/debug.h
inc/memory.h
inc/object.h
inc/scanner.h
inc/table.h
inc/value.h
inc/vm.h
)


add_executable(clox "${SOURCE}" "${HEADERS}")

target_include_directories(clox PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/inc")
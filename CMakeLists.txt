cmake_minimum_required(VERSION 3.17)
set(PICO_SDK_PATH "C:\\pico\\pico-sdk")

include(pico_sdk_import.cmake)

project(MPU9250)

pico_sdk_init()

set(CMAKE_CXX_STANDARD 17)

include_directories(src)
add_subdirectory(src)

add_executable(main main.cpp)
target_link_libraries(main pico_stdlib MPU_9250)

# enable usb output, disable uart output
pico_enable_stdio_usb(main 1)
pico_enable_stdio_uart(main 0)

# create map/bin/hex/uf2 file etc.
pico_add_extra_outputs(main)
add_library(MPU_9250 STATIC MPU9250.cpp)
target_link_libraries(MPU_9250 pico_stdlib hardware_spi pico_mem_ops)

# enable usb output, disable uart output
pico_enable_stdio_usb(MPU_9250 1)
pico_enable_stdio_uart(MPU_9250 0)

# create map/bin/hex/uf2 file etc.
#pico_add_extra_outputs(MPU_9250)
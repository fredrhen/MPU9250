add_library(MPU_9250 STATIC MPU9250.cpp)
target_link_libraries(MPU_9250 pico_stdlib hardware_spi)
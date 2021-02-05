cmake_minimum_required(VERSION 3.17)
set(PICO_SDK_PATH "C:\\pico\\pico-sdk")

include(pico_sdk_import.cmake)

project(MPU9250)

set(CMAKE_CXX_STANDARD 17)

include_directories(src)


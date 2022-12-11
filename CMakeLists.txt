cmake_minimum_required(VERSION 3.22)

set(CMAKE_TOOLCHAIN_FILE ${CMAKE_CURRENT_SOURCE_DIR}/thirdparty/stm32-cmake/cmake/stm32_gcc.cmake)

project(stm32-ws2812-cube C ASM)

set(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG} -O0 -Wall -Wextra -Werror -Wduplicated-branches \
-Wduplicated-cond -Wfloat-equal -Wshadow=compatible-local -Wcast-qual -Wconversion -Wsign-conversion \
-Wlogical-op -pedantic -g3")

set(PROJECT_SOURCES
  ${CMAKE_CURRENT_SOURCE_DIR}/src/main.c
)


add_subdirectory(target/STM32F103C8)

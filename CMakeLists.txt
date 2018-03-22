cmake_minimum_required(VERSION 3.9)
project(opencl C)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_LIBRARIES -lOpenCL)
set(CMAKE_C_FLAGS -fPIC)
set(SOURCE_FILES main.c Tools/Timer.c Tools/OpenCL_Wrapper.c Tools/Timer.h Tools/OpenCL_Wrapper.h
        OpenCL/Kernel.cl main.h)
add_executable(opencl ${SOURCE_FILES})
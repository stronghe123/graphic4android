
cmake_minimum_required(VERSION 3.4.1)

##官方标准配置
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -fno-rtti -fno-exceptions -Wall")

add_library(native-yuv2rgb
           SHARED
           src/main/cpp/native_yuv2rgb.cpp)

target_link_libraries(native-yuv2rgb
            android
            jnigraphics
            log)

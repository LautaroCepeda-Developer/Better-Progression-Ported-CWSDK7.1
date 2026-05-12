cmake_minimum_required(VERSION 3.8)

project(BetterProgression)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(CWSDK)

add_library(BetterProgression SHARED "main.cpp")

target_link_libraries(BetterProgression LINK_PUBLIC CWSDK)

target_include_directories(BetterProgression PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/CWSDK)
target_include_directories(BetterProgression PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/CWSDK/common)
target_include_directories(BetterProgression PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/CWSDK/cube)
target_include_directories(BetterProgression PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/CWSDK/gfx)
target_include_directories(BetterProgression PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/CWSDK/IDA)
target_include_directories(BetterProgression PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/CWSDK/msvc)
target_include_directories(BetterProgression PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/CWSDK/plasma)
target_include_directories(BetterProgression PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/CWSDK/steam)
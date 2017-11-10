cmake_minimum_required(VERSION 3.2.2)


file(GLOB SOURCES "AdsLib/*.cpp" "AdsLib/*.c" "AdsLib/*.hpp" "AdsLib/*.h")

add_library(AdsLib STATIC ${SOURCES})

include_directories(${CMAKE_SOURCE_DIR}/ADS/AdsLib ${CMAKE_SOURCE_DIR}/ADS/tools)

install(TARGETS AdsLib ARCHIVE DESTINATION bin 
    LIBRARY DESTINATION bin RUNTIME DESTINATION bin)

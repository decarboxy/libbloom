project(libbloom)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/murmur2)
include_directories(${CMAKE_CURRENT_SOURCE_DIR})

add_library(Murmur2 murmur2/MurmurHash2.c)

add_library(Bloom bloom.c)
target_link_libraries(Bloom Murmur2)
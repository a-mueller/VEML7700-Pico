add_library(veml7700 INTERFACE)

target_sources(veml7700 INTERFACE
  ${CMAKE_CURRENT_LIST_DIR}/src/VEML770.cpp
)

target_include_directories(veml7700 INTERFACE ${CMAKE_CURRENT_LIST_DIR}/src ${CMAKE_CURRENT_LIST_DIR}/include)

# Pull in pico libraries that we need
target_link_libraries(veml7700 INTERFACE pico_stdlib hardware_i2c)

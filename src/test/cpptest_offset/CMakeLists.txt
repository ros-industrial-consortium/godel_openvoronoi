
# The next line tells CMake and CTest about "test_minimal".
SET(test_name "cpptest_offset" )

MESSAGE(STATUS "configuring c++ test: " ${test_name})

set(SOURCE_FILES offset.cpp)
add_executable(${test_name} ${SOURCE_FILES})
add_dependencies(${test_name}  libopenvoronoi)

target_link_libraries(${test_name} libopenvoronoi )

ADD_TEST(${test_name} ${test_name})

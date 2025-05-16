cmake_minimum_required(VERSION 3.15)
project(ToyGTest LANGUAGES CXX)

enable_testing()
find_package(GTest CONFIG REQUIRED)

add_executable(unit_tests test_example.cpp)
target_link_libraries(unit_tests PRIVATE GTest::gtest_main)

include(GoogleTest)
gtest_discover_tests(unit_tests)
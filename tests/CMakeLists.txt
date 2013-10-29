enable_testing()

include_directories(${CMAKE_SOURCE_DIR})

add_executable(simple_test simple_test.cc ../base64.h)
add_test(SimpleTest simple_test)

add_custom_target(check COMMAND ${CMAKE_CTEST_COMMAND} --output-on-failure DEPENDS simple_test)

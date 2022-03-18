#-----------------------------------------------------------------

set(TARGET_NAME tests)

#-----------------------------------------------------------------

set(MODULES
  hello-lib
  gtest_main
)

#-----------------------------------------------------------------

set(TEST_FILES
  test_hello.cpp
)

#-----------------------------------------------------------------

add_executable(${TARGET_NAME}
  ${TEST_FILES}
)

#-----------------------------------------------------------------

target_link_libraries(${TARGET_NAME}
  ${MODULES}
)

target_include_directories(${TARGET_NAME}
  PRIVATE
    "${gtest_SOURCE_DIR}/include"
)

#-----------------------------------------------------------------

include(GoogleTest)
gtest_discover_tests(${TARGET_NAME})

#-----------------------------------------------------------------

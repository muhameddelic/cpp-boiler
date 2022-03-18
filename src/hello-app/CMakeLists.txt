#-----------------------------------------------------------------

set(TARGET_NAME hello-app)

#-----------------------------------------------------------------

set(SRC_FILES
  main.cpp
)

#-----------------------------------------------------------------

add_executable(${TARGET_NAME} ${SRC_FILES})

#-----------------------------------------------------------------

target_link_libraries(${TARGET_NAME}
  PRIVATE
    hello-lib
)

target_include_directories(${TARGET_NAME}
  PUBLIC
    hello-lib
)

#-----------------------------------------------------------------

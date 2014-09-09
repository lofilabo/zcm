cmake_minimum_required(VERSION 2.8)
project(rhello)

ENABLE_TESTING()
SET(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake )

SET(HDRS 
  hello.h
)

SET(SRCS
  hello.c
)

add_executable(rhello ${SRCS} ${HDRS})
target_link_libraries(rhello m ncurses)

#add_subdirectory(test)

install(
  TARGETS rhello
  RUNTIME DESTINATION bin
)

#  find_package(Doxygen)
#  if(DOXYGEN_FOUND)
#    add_custom_target(docs
#    ${DOXYGEN_EXECUTABLE} ${CMAKE_CURRENT_SOURCE_DIR}/Doxyfile
#    WORKING_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}
#    COMMENT "Generating API documentation with Doxygen" VERBATIM
#    )
#  else(DOXYGEN_FOUND)
#    message(WARNING 
#      "Couldn't find doxygen. You won't be able to generate documentation now")
#  endif(DOXYGEN_FOUND)

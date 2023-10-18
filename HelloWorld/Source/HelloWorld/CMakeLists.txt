
add_executable(HelloWorld
  HelloWorld.swift)
target_link_libraries(HelloWorld PRIVATE
  HelloWorldCore)

add_test(HelloWorld COMMAND ${CMAKE_RUNTIME_OUTPUT_DIRECTORY}/HelloWorld)
set_target_properties(HelloWorld PROPERTIES
  Swift_LANGUAGE_VERSION 4.2)

install(TARGETS HelloWorld
  DESTINATION bin
  COMPONENT exe)


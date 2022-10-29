cmake_minimum_required(VERSION 3.12)

project(
	ExampleWithLibrary
	VERSION 1.0
	LANGUAGES CXX
	DESCRIPTION "Show the naive lib-linking"
	HOMEPAGE_URL "http://vorlesung.nabla-b.engineering"
)



add_library(myLib myLib.cpp myLib.h)


add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE myLib)

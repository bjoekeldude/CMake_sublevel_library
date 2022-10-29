cmake_minimum_required(VERSION 3.12)

project(
	ExampleWithSubdirectory
	VERSION 1.0
	LANGUAGES CXX
	DESCRIPTION "Show the naive subdir inclusion"
	HOMEPAGE_URL "http://vorlesung.nabla-b.engineering"
)



add_subdirectory(${CMAKE_SOURCE_DIR}/myLibDirectory)

add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME} myLib)

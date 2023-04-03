cmake_minimum_required(VERSION 3.16)
project(NTop C)

option(ENABLE_UNICODE "Compile with Unicode support" OFF)

if(ENABLE_UNICODE)
	add_definitions(-DUNICODE -D_UNICODE)
endif()

link_libraries(shlwapi)

add_executable(NTop ntop.c util.c vi.c)

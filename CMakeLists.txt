CMAKE_MINIMUM_REQUIRED(VERSION 2.8)      
 
PROJECT(HttpServer)                                          
 
MESSAGE(STATUS "Project: HttpServer")               
MESSAGE(STATUS "Project Directory: ${PROJECT_SOURCE_DIR}")
 
SET(CMAKE_BUILE_TYPE DEBUG)               
SET(CMAKE_C_FLAGS_DEBUG "-g -Wall")          
SET(CMAKE_CXX_FLAGS_DEBUG "-g -Wall -std=c++11")

#ADD_SUBDIRECTORY(src)
ADD_SUBDIRECTORY(utility)

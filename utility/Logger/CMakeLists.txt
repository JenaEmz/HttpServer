SET(SOURCE_FILES                                  #设置变量，表示所有的源文件
Logger.cpp
)


INCLUDE_DIRECTORIES(                          #相关头文件的目录
/usr/local/include
${PROJET_SOURCE_DIR}/utility
)


LINK_DIRECTORIES(                                  #相关库文件的目录
/usr/local/lib
)
ADD_LIBRARY(Logger ${SOURCE_FILES})         #生成静态链接库libassociation.a

#TARGET_LINK_LIBRARY(association core）                #依赖的库文件 
SET_TARGET_PROPERTIES(Logger  PROPERTIES   
RUNTIME_OUTPUT_DIRECTORY> "${PROJECT_SOURCE_DIR}/lib") 
ADD_SUBDIRECTORY(test)

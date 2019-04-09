SET(SOURCE_FILES
test.cpp
)

INCLUDE_DIRECTORIES(
/usr/local/include
${PROJECT_SOURCE_DIR}/utility
${PROJECT_SOURCE_DIR}/include

)

link_directories(
/usr/local/lib
${PROJECT_SOURCE_DIR}/lib
)

ADD_EXECUTABLE(test_logger  ${SOURCE_FILES})

TARGET_LINK_LIBRARIES(test_logger
Logger
pthread
)

SET_TARGET_PROPERTIES(test_logger  PROPERTIES    #表示生成的执行文件所在路径
RUNTIME_OUTPUT_DIRECTORY  "${PROJECT_SOURCE_DIR}/bin") 

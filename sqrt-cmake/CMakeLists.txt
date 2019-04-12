#1. cmake verson，指定cmake版本 
cmake_minimum_required(VERSION 2.6)

# 2. project name  设置项目名称
PROJECT(sqrt-cmake)

# 3. head file path  设置包含的目录
INCLUDE_DIRECTORIES(
include
)

# 4. source directory   搜索当前目录下的所有.c文件
AUX_SOURCE_DIRECTORY(src DIR_SRCS)

# 5. set environment variable
SET(TEST_MATH
${DIR_SRCS}
)

# 6. add executable file
ADD_EXECUTABLE(${PROJECT_NAME} ${TEST_MATH})

# 7. add link library 设置 target 需要链接的库
TARGET_LINK_LIBRARIES(${PROJECT_NAME} m)









#1. cmake verson，指定cmake版本 
cmake_minimum_required(VERSION 2.6)

# 2. project name
PROJECT(sqrt-cmake)

# 3. head file path
INCLUDE_DIRECTORIES(
include
)

# 4. source directory
AUX_SOURCE_DIRECTORY(src DIR_SRCS)

# 5. set environment variable
SET(TEST_MATH
${DIR_SRCS}
)

# 6. add executable file
ADD_EXECUTABLE(${PROJECT_NAME} ${TEST_MATH})

# 7. add link library
TARGET_LINK_LIBRARIES(${PROJECT_NAME} m)









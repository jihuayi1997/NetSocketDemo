# CMakeList.txt: Server 的 CMake 项目，在此处包括源代码并定义
# 项目特定的逻辑。
#
cmake_minimum_required (VERSION 3.8)

# 将源代码添加到此项目的可执行文件。
project(Client)

file(GLOB_RECURSE ${PROJECT_NAME_U}_SOURCE_FILES *.cpp)
file(GLOB_RECURSE ${PROJECT_NAME_U}_HEADER_FILES *.h)

source_group("Header Files" FILES ${${PROJECT_NAME_U}_HEADER_FILES})
source_group("Source Files" FILES ${${PROJECT_NAME_U}_SOURCE_FILES})

add_executable(${PROJECT_NAME} 
    ${${PROJECT_NAME_U}_SOURCE_FILES}
    ${${PROJECT_NAME_U}_HEADER_FILES} 
)

# TODO: 如有需要，请添加测试并安装目标。

cmake_minimum_required(VERSION 2.6)
project(506_FrameField)

include("../CMakeLists.shared")

find_package(LIBCOMISO REQUIRED)

include_directories( ${LIBCOMISO_INCLUDE_DIR} )

set(SOURCES
${PROJECT_SOURCE_DIR}/main.cpp
)

add_executable(${PROJECT_NAME}_bin ${SOURCES} ${SHARED_SOURCES})
target_link_libraries(${PROJECT_NAME}_bin ${SHARED_LIBRARIES} ${LIBCOMISO_LIBRARY})

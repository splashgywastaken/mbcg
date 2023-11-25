cmake_minimum_required(VERSION 3.0...3.28)
project(mbcg VERSION 0.1.0 LANGUAGES C CXX)

find_package(glfw3 CONFIG REQUIRED)
find_package(glm CONFIG REQUIRED)
find_package(imgui CONFIG REQUIRED)
find_package(glad CONFIG REQUIRED)

add_subdirectory(src)

target_include_directories(${PROJECT_NAME} PRIVATE "${VCPKG_X64W_DIR}\\include")

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

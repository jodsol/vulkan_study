cmake_minimum_required(VERSION 3.10)
project(hello_vulkan)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Vulkan REQUIRED)
find_package(glfw3 REQUIRED)
find_package(glm REQUIRED)

add_executable(hello_vulkan gpgpu.cpp)

# Vulkan과 GLFW 라이브러리 링크
target_link_libraries(hello_vulkan 
    Vulkan::Vulkan
    glfw
    glm::glm
)
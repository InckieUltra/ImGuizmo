cmake_minimum_required(VERSION 3.10)

# 收集所有cpp文件
file(GLOB IMGUIZMO_SOURCES *.cpp)

add_library(ImGuizmo STATIC ${IMGUIZMO_SOURCES})

target_include_directories(ImGuizmo PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

# ImGuizmo 依赖 ImGui，假设上层项目会传递imgui target给它
target_link_libraries(ImGuizmo PUBLIC imgui)

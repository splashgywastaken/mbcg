add_executable(mbcg main.cpp)
target_link_libraries(
    mbcg
    PRIVATE glfw
    PRIVATE imgui::imgui
    PRIVATE glad::glad
)
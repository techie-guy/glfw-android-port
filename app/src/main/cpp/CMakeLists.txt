cmake_minimum_required(VERSION 3.4.1)

project(glfw-android)

set(GLFW_BUILD_DOCS OFF)
set(GLFW_INSTALL OFF)
set(GLFW_BUILD_EXAMPLES OFF)
set(GLFW_BUILD_TESTS OFF)
set(GLFW_BUILD_WIN32 OFF)
set(GLFW_BUILD_X11 OFF)
set(GLFW_BUILD_ANDROID ON)
set(CMAKE_CXX_STANDARD 17)

set(CMAKE_EXPORT_COMPILE_COMMANDS 1)

add_subdirectory(glfw)

set(CMAKE_SHARED_LINKER_FLAGS "${CMAKE_SHARED_LINKER_FLAGS} -u ANativeActivity_onCreate") #

# add_definitions(-DVK_USE_PLATFORM_ANDROID_KHR=1)

add_library(glfw-android SHARED main.cpp imgui/imgui.cpp imgui/imgui_demo.cpp imgui/imgui_draw.cpp imgui/imgui_tables.cpp imgui/imgui_widgets.cpp imgui/backends/imgui_impl_opengl3.cpp imgui/backends/imgui_impl_glfw.cpp)

target_include_directories(glfw-android PRIVATE ${ANDROID_NDK}/sources/android/native_app_glue imgui imgui/backends)

target_link_libraries(glfw-android glfw)

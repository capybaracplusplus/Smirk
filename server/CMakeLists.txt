cmake_minimum_required(VERSION 3.29.6)
project(Smirk)

set(CMAKE_CXX_STANDARD 23)

find_package(userver REQUIRED COMPONENTS core postgresql)

add_executable(Smirk src/main.cpp)

target_link_libraries(${PROJECT_NAME} PUBLIC userver::core userver::postgresql)
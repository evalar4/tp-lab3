# Указываем минимальную версию CMake
cmake_minimum_required(VERSION 3.10)

# Указываем имя проекта
project(solver_lib)

# Указываем стандарт C++
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Указываем директорию с исходными файлами
set(SOURCES
    solver.cpp
)

# Создаем статическую библиотеку solver_lib
add_library(solver_lib STATIC ${SOURCES})

# Указываем директории, где находятся заголовочные файлы
target_include_directories(solver_lib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})


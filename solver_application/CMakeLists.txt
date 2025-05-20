# Указываем минимальную версию CMake
cmake_minimum_required(VERSION 3.10)

# Указываем имя проекта
project(solver)

# Указываем директорию с исходными файлами
set(SOURCES
    equation.cpp
)

# Создаем исполняемый файл solver
add_executable(solver ${SOURCES})

# Указываем зависимости от библиотек
target_link_libraries(solver PRIVATE formatter_ex solver_lib)


# Указываем минимальную версию CMake
cmake_minimum_required(VERSION 3.10)

# Указываем имя проекта
project(hello_world)

# Указываем директорию с исходными файлами
set(SOURCES
    hello_world.cpp
)

# Создаем исполняемый файл hello_world
add_executable(hello_world ${SOURCES})

# Указываем зависимости от библиотек
target_link_libraries(hello_world PRIVATE formatter_ex)


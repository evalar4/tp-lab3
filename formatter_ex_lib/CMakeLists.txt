cmake_minimum_required(VERSION 3.10)

project(formatter_ex)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

set(SOURCES
    formatter_ex.cpp
)

set(FORMATTER_LIB_DIR "../formatter_lib")

add_subdirectory(${FORMATTER_LIB_DIR} formatter_lib_build)

# Создаем библиотеку formatter_ex
add_library(formatter_ex STATIC ${SOURCES})

# Указываем директории, где находятся заголовочные файлы
target_include_directories(formatter_ex PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

# Указываем зависимость от библиотеки formatter
target_link_libraries(formatter_ex PUBLIC formatter)


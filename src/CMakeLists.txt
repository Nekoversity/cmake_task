# Определение минимальной версии сборщика, если меньше -> аварийный выход
cmake_minimum_required(VERSION 3.10)

# Определение стандарта
set(CMAKE_CXX_STANDARD 14)

# Определение исполняемого файла, его имени
add_executable(cmake_task main.cpp)

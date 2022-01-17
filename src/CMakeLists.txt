# Определение минимальной версии сборщика, если меньше -> аварийный выход
cmake_minimum_required(VERSION 3.10)

# Имя проекта
project(cmake_task)

# Установка переменной со списком исходников для исполняемого файла
set(SOURCE_EXE main.cpp)

# Тоже самое, но для библиотеки
set(SOURCE_LIB kat.cpp)

# Добавление статической библиотеки с именем kat
add_library(kat STATIC ${SOURCE_LIB})

# Создает исполняемый файл с именем main
add_executable(main ${SOURCE_EXE})

# Привязка библиотеки к исполняемому файлу
target_link_libraries(main kat)

# Определение стандарта
set(CMAKE_CXX_STANDARD 14)

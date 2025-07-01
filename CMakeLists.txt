cmake_minimum_required(VERSION 3.10)

project(raylib_project C)

# Spécifie le standard C
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)

# Trouve la bibliothèque Raylib installée sur le système
find_package(raylib REQUIRED)

# Inclut les headers personnalisés du projet
include_directories(include)

# Ajoute les fichiers source
add_executable(${PROJECT_NAME}
    src/main.c
    src/player.c
    src/utils.c
)

# Lie l'exécutable aux bibliothèques nécessaires
target_link_libraries(${PROJECT_NAME} raylib m)
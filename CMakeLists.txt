cmake_minimum_required(VERSION 3.10)
project(raylib_project C)

# Version du standard C
set(CMAKE_C_STANDARD 99)

# Rechercher Raylib installée sur le système (après sudo make install)
find_package(raylib REQUIRED)

# Inclure les headers personnalisés du dossier include/
include_directories(include)

# Ajouter les fichiers source
add_executable(${PROJECT_NAME}
    src/main.c
    src/player.c
    src/utils.c
)

# Lier les bibliothèques nécessaires
target_link_libraries(${PROJECT_NAME} raylib m)

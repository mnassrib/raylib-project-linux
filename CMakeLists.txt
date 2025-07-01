cmake_minimum_required(VERSION 3.10)

# Déclare le projet C en spécifiant le nom
project(raylib_project C)

# Utiliser le standard C99 (obligatoire pour Raylib)
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)

# Recherche Raylib dans le système (fichier raylibConfig.cmake requis)
find_package(raylib REQUIRED)

# Inclut les headers de ton projet (dans le dossier include/)
include_directories(include)

# Liste des fichiers sources à compiler
add_executable(${PROJECT_NAME}
    src/main.c
    src/player.c
    src/utils.c
)

# Lie l'exécutable aux bibliothèques nécessaires :
# - raylib : bibliothèque principale
# - m : bibliothèque mathématique standard (uniquement requise sous Linux)
target_link_libraries(${PROJECT_NAME} raylib m)
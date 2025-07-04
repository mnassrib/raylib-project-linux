# 🎮 Raylib Project (Linux / WSL)

Ce projet montre comment utiliser la bibliothèque [Raylib](https://www.raylib.com/) pour créer un programme en C avec une structure propre basée sur **CMake**. Il est conçu pour être compilé sous **Linux ou WSL**, avec prise en charge de l’intégration continue sur GitHub Actions.

---

## 📁 Structure du projet

```

raylib-project-linux/
├── CMakeLists.txt           # Configuration du projet (CMake)
├── src/                     # Fichiers source (.c)
│   ├── main.c
│   ├── player.c
│   └── utils.c
├── include/                 # Fichiers d’en-tête (.h)
│   ├── player.h
│   └── utils.h
├── build/                   # Dossier de compilation (généré)
└── .github/
    └── workflows/
        └── ci-linux.yml     # GitHub Actions (Linux)

````

---

## ⚙️ Compilation sous Linux / WSL

### 📌 Prérequis

- Système Linux (Ubuntu recommandé) ou WSL
- Raylib installé manuellement (ou via package)
- `gcc`, `cmake`, et les dépendances de développement installés :

```bash
sudo apt update
sudo apt install git cmake build-essential \
libasound2-dev libx11-dev libxcursor-dev \
libxrandr-dev libxi-dev libgl1-mesa-dev \
libxinerama-dev libxss-dev libwayland-dev \
libpulse-dev libxext-dev
````

### 🔧 Compiler Raylib (si non installé via apt)

```bash
git clone https://github.com/raysan5/raylib.git
cd raylib
mkdir build && cd build
cmake ..
make
sudo make install
```

---

## 🚀 Compilation du projet

```bash
# Cloner ce dépôt
git clone https://github.com/mnassrib/raylib-project-linux.git
cd raylib-project

# Créer un dossier de build
mkdir build && cd build

# Configurer le projet
cmake ..

# Compiler
make

# Lancer l'exécutable
./raylib_project
```

---

## ✅ Intégration Continue

Ce projet est compilé automatiquement sur **Ubuntu Linux** à chaque `push` via GitHub Actions :

![CI Status](https://github.com/mnassrib/raylib-project-linux/actions/workflows/ci-linux.yml/badge.svg)

---
## 🚀 Télécharger l’exécutable précompilé

Après chaque publication (tag Git), une version précompilée de l'exécutable est disponible :

1. Accède à la page des **Releases** ici :
   🔗 [https://github.com/mnassrib/raylib-project-linux/releases](https://github.com/mnassrib/raylib-project-linux/releases)
2. Télécharge le fichier **raylib\_project** (ou `.exe` selon l’OS) de la dernière version.
3. Exécute directement en local le programme sans recompiler.

---

## 🧠 Ressources utiles

* [Raylib – Documentation](https://www.raylib.com/)
* [CMake - Documentation](https://cmake.org/documentation/)

---

## 📄 Licence

Ce projet est librement utilisable à des fins pédagogiques et de formation.

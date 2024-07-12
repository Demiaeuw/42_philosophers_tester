# Philosopher Tester

Bienvenue dans le repository du Philosopher Tester. Ce projet est conçu pour automatiser les tests de votre implémentation du problème des philosophes mangeurs. Il vérifie le comportement de votre programme en termes de synchronisation, de gestion des threads et de gestion des ressources.

## Contenu

  **CMakeLists.txt** : Configuration de CMake pour compiler et exécuter les tests.
  **check_valgrind.py** : Script Python pour vérifier les fuites de mémoire à l'aide de Valgrind.
  **timeout_validator.py** : Script Python pour valider les tests qui doivent s'arrêter après un certain temps.
  **README.md** : Ce fichier, expliquant comment utiliser le tester.

## Utilisation

### 1. Configuration du Projet

Clonez ce repository dans le répertoire test de votre projet de philosophes. Votre arborescence devrait ressembler à ceci :

objectif

```
votre_projet/
│
├── Tous vos fichiers
├── MAKEFILE
├── philosopher
└── test/
    ├── CMakeLists.txt
    ├── check_valgrind.py
    ├── timeout_validator.py
```

### 2. Compilation et Exécution des Tests

Étape 1 : Création du répertoire de build

Naviguez dans le répertoire test et créez un répertoire build pour les fichiers de build.

```
mkdir build
cd build
```

Étape 2 : Configuration avec CMake

Configurez votre projet avec CMake en exécutant la commande suivante :
```
cmake ..
```
Étape 3 : Compilation

Compilez le projet en utilisant make :
```
make
```
Étape 4 : Exécution des Tests

Exécutez les tests en utilisant ctest :
```
ctest
```
### 3. Détails des Scripts de Test

check_valgrind.py

Ce script utilise Valgrind pour vérifier les fuites de mémoire. Il doit être exécuté avec les arguments de Valgrind suivis de votre exécutable et de ses arguments.

Exemple :
```
python3 check_valgrind.py valgrind --leak-check=full ./votre_executable 5 800 200 200
```

timeout_validator.py

Ce script valide si un test dure plus ou moins longtemps qu'un temps donné. Il arrête l'exécution de votre programme après le temps spécifié et valide le test en fonction de la durée.

Exemple :
```
python3 timeout_validator.py 20 ./votre_executable 5 800 200 200
```

## Conclusion

Ce repository fournit un ensemble d'outils pour automatiser et valider les tests de votre implémentation des philosophes mangeurs. Assurez-vous que votre projet est structuré correctement et suivez les étapes fournies pour configurer et exécuter les tests.

## Attention

!!! Ce tester ne doit pas remplacer vos tests !!!


---
---

# Philosopher Tester

Welcome to the Philosopher Tester repository. This project is designed to automate the testing of your implementation of the Dining Philosophers problem. It checks the behavior of your program in terms of synchronization, thread management, and resource handling.

## Contents

   **CMakeLists.txt** : CMake configuration to compile and run the tests.
   **check_valgrind.py** : Python script to check for memory leaks using Valgrind.
   **timeout_validator.py** : Python script to validate tests that should stop after a certain time.
   **README.md** : This file, explaining how to use the tester.

## Usage
1. Project Setup

Clone this repository into the test directory of your philosophers project. Your directory structure should look like this:

objective:
```
your_project/
│
├── All your Documents
├── MAKEFILE
├── philosopher
└── test/
    ├── CMakeLists.txt
    ├── check_valgrind.py
    ├── timeout_validator.py
```
2. Compilation and Running Tests
Step 1: Create the Build Directory

Navigate to the test directory and create a build directory for the build files.
```
mkdir build
cd build
```

Step 2: Configuration with CMake

Configure your project with CMake by running the following command:
```
cmake ..
```

Step 3: Compilation

Compile the project using make:
```
make
```

Step 4: Running Tests

Run the tests using ctest:
```
ctest
```

3. Test Scripts
check_valgrind.py

This script uses Valgrind to check for memory leaks. It should be run with Valgrind arguments followed by your executable and its arguments.

Example:
```
python3 check_valgrind.py valgrind --leak-check=full ./your_executable 5 800 200 200
```
timeout_validator.py

This script validates if a test runs more or less than a given time. It stops your program's execution after the specified time and validates the test based on the duration.

Example:
```
python3 timeout_validator.py 20 ./your_executable 5 800 200 200
```
## Conclusion

This repository provides a set of tools to automate and validate the testing of your Dining Philosophers implementation. Ensure your project is correctly structured and follow the provided steps to set up and run the tests.

## Warning

!!! This tester should not replace your own tests !!!

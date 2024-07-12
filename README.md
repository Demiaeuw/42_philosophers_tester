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

bash

mkdir build
cd build

Étape 2 : Configuration avec CMake

Configurez votre projet avec CMake en exécutant la commande suivante :

bash

cmake ..

Étape 3 : Compilation

Compilez le projet en utilisant make :

bash

make

Étape 4 : Exécution des Tests

Exécutez les tests en utilisant ctest :

bash

ctest

### 3. Scripts de Test

check_valgrind.py

Ce script utilise Valgrind pour vérifier les fuites de mémoire. Il doit être exécuté avec les arguments de Valgrind suivis de votre exécutable et de ses arguments.

Exemple :

bash

python3 check_valgrind.py valgrind --leak-check=full ./votre_executable 5 800 200 200

timeout_validator.py

Ce script valide si un test dure plus ou moins longtemps qu'un temps donné. Il arrête l'exécution de votre programme après le temps spécifié et valide le test en fonction de la durée.

Exemple :

bash

python3 timeout_validator.py 20 ./votre_executable 5 800 200 200

## Conclusion

Ce repository fournit un ensemble d'outils pour automatiser et valider les tests de votre implémentation des philosophes mangeurs. Assurez-vous que votre projet est structuré correctement et suivez les étapes fournies pour configurer et exécuter les tests.

## Attention

!!! Ce tester ne doit pas remplacer vos tests !!!

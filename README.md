# 🤖 Simulation de Navigation d'un Rover sur Terrain à Coûts

[![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)](https://en.wikipedia.org/wiki/C_(programming_language))
[![CMake](https://img.shields.io/badge/CMake-064F8C?style=for-the-badge&logo=cmake&logoColor=white)](https://cmake.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

> Simulateur de trajectoire et de navigation autonome pour un robot explorateur martien (Rover). Implémenté en **C** avec gestion de mémoire dynamique, files de priorités et calcul de chemins optimaux sur des cartes topographiques à coûts hétérogènes.

---

## 🎯 Contexte & Objectifs

L'objectif du projet est de simuler et d'optimiser les déplacements d'un robot autonome sur une grille cartographique représentant un terrain accidenté :
- **Types de surfaces variés :** Plaines, roches, sables mouvants, cratères, obstacles infranchissables, chacun imposant un coût de déplacement spécifique.
- **Calcul de trajectoires :** Détermination de la séquence de mouvements optimale (`Avancer`, `Reculer`, `Tourner à gauche`, `Tourner à droite`) pour atteindre la cible avec le coût énergétique minimal.
- **Structures de données avancées en C :** Files (*queues*), listes chaînées, matrices dynamiques et gestion rigoureuse de la mémoire sans fuites.

---

## 📁 Structure du Projet

```text
├── CMakeLists.txt         # Configuration de compilation CMake
├── main.c                 # Point d'entrée et boucle principale de simulation
├── loc.h / loc.c          # Types de données géographiques (coordonnées, orientation)
├── map.h / map.c          # Chargement, parsing et manipulation des cartes
├── moves.h / moves.c      # Définition des mouvements et application cinématique
├── select_move.c          # Algorithme de sélection et heuristique de décision
├── queue.h / queue.c      # Implémentation de file FIFO pour la file de mouvements
├── list.h / list.c        # Listes dynamiques pour l'historique des positions
├── counter.h / counter.c  # Compteurs de métriques et coûts cumulés
├── maps/                  # Cartes d'entraînement et de test (.map)
│   ├── training.map
│   └── example1.map
```

---

## 🛠️ Compilation & Exécution

### Prérequis
- Compilateur C (GCC, Clang)
- CMake 3.10+

### Compilation avec CMake
```bash
# Cloner le dépôt
git clone https://github.com/TonneauBenjamin/Projet-Rover.git
cd Projet-Rover

# Créer le répertoire de build et compiler
mkdir build && cd build
cmake ..
make
```

### Exécution
```bash
./Projet_Rover
```

---

## 👥 Équipe du Projet

Projet d'ingénierie réalisé à l'**EFREI Paris** par :
- **Benjamin Tonneau**
- Arthur Boutelier
- Victor Proffit

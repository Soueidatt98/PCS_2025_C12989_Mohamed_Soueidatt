# Étude comparative : Python vs Julia vs Mojo  
*(Semaine 1 – Travaux complémentaires)*

---

## 1. Pourquoi comparer ?  
- **Python** reste le langage de référence en science des données grâce à son écosystème gigantesque (NumPy, pandas, PyTorch…).  
- **Julia** promet la vitesse du C avec la syntaxe d’un script, sans avoir à passer en C/Fortran pour accélérer.  
- **Mojo** (2023-25) vise la même ergonomie que Python **mais** avec des performances natives CPU + GPU pour l’IA.   

Comprendre leurs forces/faiblesses aide à choisir la bonne techno (ou le bon mélange) pour un projet donnée.

---

## 2. Vue d’ensemble rapide

| Critère | **Python 3.12** | **Julia 1.11** | **Mojo 0.8** |
|---|---|---|---|
| Typage | Dynamique | Dynamique + optionnel statique | Statique par défaut (superset Python) |
| Compilation | Interprété + bytecode (CPython), JIT partiel (3.13 « nogil ») | JIT LLVM à la volée | Ahead-of-Time & JIT, LLVM |
| Vitesse brute | Lente sans libs natives ; s’améliore avec Cython, Numba | Près du C dès l’écriture | Annoncée proche du C/Metal/GPU |
| Écosystème | ***énorme*** (PyPI > 500 k paquets) | Plus jeune, niche mais grandit (packages ≈ 11 k)  | Tout neuf, principalement IA / HPC |
| Multi-threads | GIL (levé partiellement 3.13) | Pas de GIL, scheduling coopératif | Pas de GIL, parallélisme fin |
| GPU natif | via libs (PyTorch, JAX, CuPy) | CUDA.jl, AMDGPU.jl | Intégré (Metal, CUDA) |
| Apprentissage | Facile, docs abondantes | Facile pour débuter, plus dur pour méta-programmation | Syntaxe proche Python, docs limitées |
| Maturité | 30 ans, stable | 13 ans, stable | < 3 ans, encore instable |

---

## 3. Performances (benchmarks synthèse)

- **Python nu** est ~10–100× plus lent que Julia sur boucles numériques pures.  
- Avec **NumPy** (appel C en vectoriel) Python rejoint souvent Julia sur opérations matricielles simples. 
- **Mojo** démos officielles : kernels AI 20 000× plus rapides que Python pur, 5–10× plus rapides que NumPy/TensorFlow sur GPU, mais dispo limitée ; difficile de reproduire publiquement (2025).  

---

## 4. Cas d’usage typiques

| Besoin | Langage conseillé |
|---|---|
| Prototyper vite, énormes libs disponibles, scripting système | **Python** |
| Algèbre linéaire lourde, simulations et PDEs haute perf, code unique production-recherche | **Julia** |
| Kernels d’entraînement IA maison, compilation vers CPU + GPU sans écrire du C++/CUDA, envie d’une syntaxe Python | **Mojo** (encore expérimental) |

---

## 5. À connaître si on vient de Python

### Passer à Julia  
- Syntaxe proche (`for`, `if`, comprehensions), pas d’indentation stricte.  
- Penser **types concrets** pour la perf : éviter `Any`.  
- Premier appel à une fonction compile (latence) → ↗ temps de démarrage.

### Essayer Mojo  
- Fichiers `.mojo` acceptent du “Python pur” + annotations `fn`, `struct`.  
- Objets Python courants importables (`from python import numpy as np`).  
- Actuellement accès via la **Mojo Playground** (cloud) ou build source Linux.

---

## 6. Limites et points de vigilance

| Langage | Bémols actuels |
|---|---|
| Python | GIL, perfs boucles, dépendance à C/Fortran pour accélérer. |
| Julia | Démarrage lent (compilation ; « time-to-first-plot »), écosystème plus petit, changelog parfois cassant. |
| Mojo | Jeune ; écosystème quasi vide, doc incomplète, licences encore susceptibles d’évoluer, pas de Windows officiel (mi-2025). |

---

## 7. Conclusion personnelle  
Je reste **intermédiaire Python** : sa simplicité et ses bibliothèques me suffisent souvent.  
Cependant :

* **Julia** m’attire pour les simulations où chaque ms compte ; son absence de GIL et ses macros sont puissants.  
* **Mojo** pourrait résoudre le « two-language problem » (Python + C/CUDA), mais il faut attendre que la langue et les outils mûrissent.

En 2025, la bonne stratégie semble donc :

1. **Prototyper** et manipuler les données en Python.  
2. **Optimiser** les sections critiques soit via **NumPy/Cython**, soit en **Julia** ou **Mojo** quand la stabilité le permettra.  


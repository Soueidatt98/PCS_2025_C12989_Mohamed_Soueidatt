# Semaine 9 - Resume personnel
*Scientific Computing with Python, 2e edition (Fuhrer - Verdier - Solem)*

---

## 1. Chapitre 18 : Python for Parallel Computing
- Le calcul parallele exploite plusieurs coeurs ou plusieurs machines.
- MPI organise les programmes en processus identifies par un rang.
- `mpi4py` donne acces aux operations MPI depuis Python.
- La communication point-a-point envoie des donnees d'un processus a un autre.
- Les communications collectives comme `scatter`, `gather`, `reduce` et `bcast` structurent les echanges.
- Les communications bloquantes et non bloquantes ont des comportements differents et doivent etre choisies selon le besoin.

## 2. Chapitre 19 : Comprehensive Examples
- Le chapitre rassemble plusieurs notions du livre dans des exemples plus longs.
- L'exemple des polynomes met en pratique classes, methodes speciales, interpolation et representation des coefficients.
- Les bases monomiale, Newton et Lagrange donnent plusieurs facons de representer un meme polynome.
- Le spectral clustering utilise les valeurs/vecteurs propres pour separer des donnees en groupes.
- Les problemes a valeurs initiales relient classes, fonctions, iterateurs et methodes numeriques.
- Ces exemples montrent comment construire des structures reutilisables au lieu de simples scripts ponctuels.

## 3. Ce que je maitrise deja
- Les bases de l'algebre lineaire avec NumPy.
- La creation de classes et l'evaluation de fonctions numeriques.

## 4. Notions a revoir / approfondir
- Les changements de base pour les polynomes.
- La communication MPI et la decomposition d'un probleme en taches paralleles.
- Les tests sur des classes numeriques plus longues.

## 5. Codes realises
Les exercices associes au chapitre 19 sont disponibles dans `Notebooks/Exercices_Chap19.ipynb`. Le chapitre 18 ne contient pas de section d'exercices.

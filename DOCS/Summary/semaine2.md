# Semaine 2 – Résumé personnel  
*Scientific Computing with Python, 2ᵉ édition (Führer • Verdier • Solem)*

---

## 1. Chapitre 4 : Linear Algebra - Arrays  

### 1.1 Vectors and Matrices  
- Utilisation de la fonction `array` pour créer des vecteurs et matrices.  
- Les opérations arithmétiques sont réalisées élément par élément.  
- Exemple : multiplication scalaire et combinaison linéaire.

### 1.2 Mathematical Preliminaries  
- Les tableaux sont traités comme des fonctions en mathématiques.  
- Les opérations élément par élément sont courantes, et `dot` est utilisé pour les produits scalaires et matriciels.

### 1.3 Accessing Array Entries  
- L’indexation et les tranches sont similaires à celles des listes Python mais appliquées à des matrices.  
- Accéder aux éléments via une ou deux indices.

### 1.4 Linear Algebra Methods in SciPy  
- Utilisation de `scipy.linalg` pour des tâches comme la décomposition LU, la solution de systèmes linéaires, et la décomposition en valeurs singulières (SVD).  
- Méthodes pour résoudre des systèmes d'équations linéaires et problèmes de moindres carrés.

---

## 2. Chapitre 5 : Advanced Array Concepts  

### 2.1 Array Views and Copies  
- Un *view* est une vue partagée des données d'un tableau, contrairement à une *copie* qui duplique les données.  
- Les vues permettent de manipuler directement les données sans les dupliquer, ce qui améliore les performances.

### 2.2 Comparing Arrays  
- Utilisation de tableaux booléens pour effectuer des comparaisons entre des tableaux.  
- Comparaison d'égalité et opérations booléennes sur les tableaux.

### 2.3 Performance and Vectorization  
- Remplacer les boucles Python lentes par des opérations vectorisées avec NumPy pour améliorer les performances.  
- Exemple de vectorisation d’une fonction pour accélérer son exécution.

### 2.4 Broadcasting  
- Le *broadcasting* permet d’effectuer des opérations entre des tableaux de formes différentes, en ajustant automatiquement leurs dimensions.

### 2.5 Sparse Matrices  
- Les matrices creuses sont utilisées lorsque la majorité des éléments sont nuls.  
- Trois formats principaux sont disponibles : CSR (Compressed Sparse Row), CSC (Compressed Sparse Column), et LIL (List of Lists).

---

## 3. Ce que je maîtrise déjà  
- Connaissances de base sur les tableaux en Python avec NumPy.  
- Notions de matrices et produits scalaires.

## 4. Notions à revoir / approfondir  
- Concepts avancés des matrices creuses et du broadcasting.  
- Techniques de vectorisation et amélioration des performances avec SciPy.

---

## 5. Codes réalisés  
Les exercices associés aux chapitre 4 sont disponibles dans `Notebooks/exercices_Chap4.ipynb`, Pour le Chapitre 5 il n'y a pas d'exercice dans le chapitre.

---


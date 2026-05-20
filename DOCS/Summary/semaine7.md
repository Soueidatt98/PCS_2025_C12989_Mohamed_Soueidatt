# Semaine 7 - Resume personnel
*Scientific Computing with Python, 2e edition (Fuhrer - Verdier - Solem)*

---

## 1. Chapitre 14 : Input and Output
- Les fichiers se manipulent avec `open`, idealement dans un bloc `with`.
- Les modes (`r`, `w`, `a`, `b`) indiquent lecture, ecriture, ajout et binaire.
- Un fichier texte est iterable ligne par ligne, ce qui evite de tout charger en memoire.
- NumPy propose `savetxt` et `loadtxt` pour les donnees numeriques simples.
- `pickle` et `shelve` sauvegardent des objets Python.
- Des modules specialises lisent aussi les fichiers Matlab et les images.

## 2. Chapitre 15 : Testing
- Les tests manuels sont utiles au debut, mais les tests automatiques sont plus fiables.
- Un test verifie une propriete attendue avec `assert` ou un framework de test.
- Un test unitaire cible une petite fonction; un test fonctionnel verifie un comportement plus global.
- Les algorithmes numeriques se testent souvent avec des tolerances (`allclose`).
- Le chronometrage permet de comparer plusieurs implementations et de reperer les goulots d'etranglement.
- Un context manager peut mesurer proprement le temps d'execution d'un bloc.

## 3. Ce que je maitrise deja
- Sauvegarder et relire de petits fichiers.
- Ecrire des tests simples avec `assert`.

## 4. Notions a revoir / approfondir
- Tester les resultats numeriques avec des tolerances adaptees.
- Differencier test unitaire et test fonctionnel.
- Mesurer les performances sans tirer de conclusion a partir d'une seule execution.

## 5. Codes realises
Les exercices associes au chapitre 15 sont disponibles dans `Notebooks/Exercices_Chap15.ipynb`. Le chapitre 14 ne contient pas de section d'exercices.

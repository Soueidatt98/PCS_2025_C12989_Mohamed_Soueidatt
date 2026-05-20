# Semaine 4 - Resume personnel
*Scientific Computing with Python, 2e edition (Fuhrer - Verdier - Solem)*

---

## 1. Chapitre 8 : Classes
- Les classes permettent de regrouper des donnees et les fonctions qui les manipulent.
- La methode `__init__` initialise les attributs; `self` represente l'objet courant.
- Les methodes speciales (`__add__`, `__radd__`, `__contains__`, `__call__`, etc.) donnent aux objets un comportement proche des types natifs.
- `property` sert a controler des attributs dependants les uns des autres.
- Les attributs de classe, les methodes de classe et l'heritage permettent de partager du comportement.
- L'encapsulation aide a separer l'interface publique de l'organisation interne.
- Une classe peut aussi jouer le role de decorateur, par exemple pour compter les appels d'une fonction.

## 2. Chapitre 9 : Iterating
- Une boucle `for` parcourt un objet iterable; `break`, `continue` et `else` controlent le deroulement.
- Un generateur avec `yield` produit les valeurs une par une, sans stocker toute la liste.
- Les iterateurs sont utiles pour les suites numeriques, les sommes, les methodes iteratives et les suites infinies.
- `itertools` fournit des outils comme `count`, `islice`, `cycle` et `takewhile`.
- Les expressions generatrices ressemblent aux comprehensions de listes mais sont paresseuses.
- Les boucles infinies doivent avoir une condition d'arret claire ou une limite maximale.

## 3. Ce que je maitrise deja
- Definition simple de classes et utilisation des methodes speciales.
- Boucles `for`, generateurs simples et expressions generatrices.

## 4. Notions a revoir / approfondir
- Bien distinguer attributs d'instance et attributs de classe.
- Eviter les recursions ou iterateurs infinis sans garde-fou.
- Comprendre les operations inverses comme `__radd__`.

## 5. Codes realises
Les exercices associes aux chapitres 8 et 9 sont disponibles dans `Notebooks/Exercices_Chap8.ipynb` et `Notebooks/Exercices_Chap9.ipynb`.

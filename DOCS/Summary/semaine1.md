# Semaine 1 – Résumé personnel  
*Scientific Computing with Python, 2ᵉ édition (Führer • Verdier • Solem)*

---

## 1. Chapitre 1 : *Getting Started*  
- **Installation rapide** : Anaconda + Spyder + IPython. Je retiens qu’une distribution isolée évite de casser le système.  
- **Bases du langage** : variables sans typage explicite, `if`, boucles `for`, fonctions avec `def`.  
- **Scripts et modules** : `%run monscript.py` dans IPython ; `import` ou `from … import` pour réutiliser ses fonctions.  
- **Idées clés** : travailler pas à pas dans la console, puis regrouper dans des scripts propres.

## 2. Chapitre 2 : *Variables and Basic Types*  
- **Types numériques** : `int` illimité, `float` (64 bits, attention aux arrondis), `complex` avec le suffixe `j`.  
- **Pièges flottants** : `0.4 - 0.3 != 0.1` ; mieux vaut `math.isclose` .  
- **Booléens** : `True`, `False`, opérateurs `and`, `or`, `not`. Casting implicite dans les conditions.  
- **Chaînes** : guillemets simples/doubles, chaînes brutes `r"..."`, formatage `f"{x:.2f}"`.  
- **Message principal** : bien connaître les types évite beaucoup d’erreurs de débutant.

## 3. Chapitre 3 : *Container Types*  
- **Listes** : index 0-based, slices `L[i:j]`, compréhension `[f(x) for x in L]`.  
- **Tableaux NumPy** : mêmes crochets mais opérations élément-par-élément et stockage homogène.  
- **Tuples** (immuables), **dictionnaires** (clé → valeur), **sets** (ensemble sans doublon).  
- **Conversions** : `list()`, `tuple()`, `set()`, etc.

---

## 4. Ce que je maîtrise déjà  
- Logique de base, boucles, fonctions : je comprends le **principe** même si certains mots-clé (`with`, `yield`…) me reviennent lentement.  
- Travaux antérieurs avec Jupyter : je sais exécuter des cellules, installer des paquets, sauver un notebook.  
- Opérations vectorielles élémentaires dans NumPy.

## 5. Notions à revoir / approfondir  
- Syntaxes que j’ai oubliées : slicing avancé (`a[:, ::-1]`), *list/dict comprehensions* imbriquées, *context managers* (`with open(...)`).  
- Stratégies d’optimisation : éviter les boucles Python pures, profiler (`%timeit`), diffusion NumPy.  
- Precisíon des virgules flottantes et critères d’égalité (`math.isclose`).

---

## 6. Codes réalisés  
- **Ch. 2 (exercices 1-6) :** `Notebooks/Exercices_Chap2.ipynb`, un exo par cellule.  
- **Ch. 3 (exercices 1-8) :** `Notebooks/Exercices_Chap3.ipynb`, idem.

---

## 7. Réflexion de fin de semaine

### 7.1 Ce que nous avons fait  
- Discussion générale sur les langages de programmation.  
- Focus : Python et ses différences.  
- Découverte rapide de **Julia** et **Mojo**.

### 7.2 Ce que j’ai appris  
- Julia et Mojo existent et visent de meilleures perfs pour l’IA que Python.  
- Pourquoi Python reste populaire malgré tout (écosystème, simplicité).

### 7.3 Mes attentes  
- Voir des exemples concrets où NumPy ralentit et comment Julia / Mojo font mieux.  
- Apprendre à profiler mon code Python.

### 7.4 Difficultés rencontrées  
- Retrouver certaines syntaxes oubliées après une longue pause.  
- Bien formuler les différences entre les trois langages sans jargon.

---

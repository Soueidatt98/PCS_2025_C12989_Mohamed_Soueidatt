# Preserving Privacy in Arabic Judgments – Synthèse

## 1. Problématique  
La multiplication des jugements rendus par les tribunaux marocains (plus de trois millions de dossiers par an) exige un accès élargi aux décisions pour assurer la cohérence de la jurisprudence. Aujourd’hui, l’anonymisation est effectuée manuellement par un greffier qui remplace les données personnelles (noms, adresses, dates de naissance, numéros de dossier, CIN, etc.) par « XXXX », une procédure lente, sujette aux erreurs et à des fuites potentielles de données sensibles. De plus, les systèmes de reconnaissance d’entités nommées (NER) existants en arabe se focalisent sur des entités générales et ignorent des entités juridiques spécifiques (numéro de dossier, code d’identité nationale), faute de corpus spécialisés.

## 2. Approche proposée  
Les auteurs développent un système en deux volets :  
1. **Extracteur de données personnelles** basé sur le NER : un modèle profond identifie dans le texte les noms propres, adresses, dates, numéros de dossier et codes d’identité. Le modèle est entraîné sur un *Arabic Legal Corpus* annoté manuellement.  
2. **Module de substitution** en Python : il remplace chaque entité détectée par « XXXX » pour produire une version anonymisée du jugement.

Le système obtient un F1‑score de **96,14 %** sur le corpus juridique créé et jusqu’à **95,77 %** sur le corpus ANERCorp, montrant sa robustesse dans des contextes variés.

## 3. Technologies utilisées  
- **Embeddings lexicales hybrides** :  
  - **BERT arabe** (contextualisé) et **FastText** (indépendant du contexte) pour la représentation au niveau des mots.  
  - **CNN de caractères** pour capturer la morphologie arabe.  
- **Encodeur de contexte** : réseau **Bi‑LSTM** suivi de deux réseaux **FFNN** pour encoder début et fin des segments.  
- **Classifieur Biaffine** pour prédire le type d’entité, optimisé par *softmax cross‑entropy*.  
- **Scripts Python** auxiliaires : `extract_parts.py`, `combine.py`, `process.py` pour la construction du corpus, et un module de remplacement pour l’anonymisation.  

## 4. Perspectives de recherche  
Les auteurs identifient deux axes majeurs :  
1. **Extension des entités reconnues** : intégrer la plaque d’immatriculation dans les jugements de circulation en enrichissant le corpus avec un plus grand nombre de décisions routières.  
2. **Moteur de recherche indexé** : accélérer la recherche dans les bases de jugements (actuellement ralentie par un SGBD relationnel) via l’extraction de mots‑clés BERT et des index optimisés.  

---

*Référence principale* : El Moussaoui T., Chakir L., Boumhidi J. « Preserving Privacy in Arabic Judgments: AI‑Powered Anonymization For Enhanced Legal Data Privacy ». *IEEE Access* (2023). DOI : [10.1109/ACCESS.2023.3324288](https://doi.org/10.1109/ACCESS.2023.3324288)


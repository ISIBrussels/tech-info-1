# Séance 4 — Exercices

[← Retour à l’accueil](../../index.html) · [Slides du cours](cours_seance_04.html)

## Objectif
S’exercer sur : boucles `for` et fonctions *built-in*.

## Énoncés

### A. Boucles `for`

#### 1. Somme des entiers de 1 à `n`

Écrivez une fonction qui prend un entier `n` et renvoie la somme des entiers de `1` à `n`.

#### 2. Liste d'entiers entre deux bornes

Écrivez une fonction qui prend deux entiers `start_value` et `end_value` et renvoie une liste contenant tous les entiers **strictement** entre ces deux valeurs (bornes exclues). Par exemple, pour `2` et `7`, on attend `[3, 4, 5, 6]`.

#### 3. Moyenne des éléments d'une liste

Écrivez une fonction qui prend une liste de nombres et renvoie la moyenne de ses éléments.

#### 4. Filtrer les multiples d'un nombre

Écrivez une fonction qui prend en entrée une liste d'entiers et un nombre `n`, et retourne une nouvelle liste contenant uniquement les éléments de la liste d'origine qui sont des multiples de `n`.

#### 5. Index des nombres impairs

Écrivez une fonction qui prend une liste d'entiers et renvoie une liste contenant les index de tous les nombres impairs dans la liste.

#### 6. Mot avec le plus de voyelles

Écrivez une fonction qui prend en entrée une liste de mots et retourne celui qui contient le plus de voyelles (`a`, `e`, `i`, `o`, `u`).

#### 7. Combinaisons de deux listes

Écrivez une fonction qui prend en entrée deux listes d'éléments et retourne une nouvelle liste contenant toutes les combinaisons possibles d'un élément de la première liste avec un élément de la deuxième.

#### 8. Validation des mots de passe

Écrivez une fonction qui prend une liste de mots de passe et renvoie une nouvelle liste indiquant, pour chaque mot de passe, s'il répond aux critères suivants :

- contient au moins une majuscule ;
- contient au moins un chiffre ;
- fait au moins 8 caractères.

#### 9. Éléments manquants dans une plage

Écrivez une fonction qui prend une liste d'entiers et vérifie s'il manque des nombres pour qu'elle forme une plage continue. Par exemple, `[3, 5, 4, 1]` est complet, mais `[3, 5, 1]` ne l'est pas.

#### 10. Classement des scores sans tri intégré

Créez une fonction qui prend en entrée une liste de scores (nombres entiers) et retourne une liste des scores triés par ordre décroissant, en implémentant vous-même la logique de tri (comparaisons et réorganisation des éléments), sans vous appuyer sur un mécanisme du langage qui effectue déjà tout le tri automatiquement.

### B. D'autres exercices

#### 11. Présence de mots longs

Écrivez une fonction qui prend une liste de mots et renvoie `True` si au moins un mot fait plus de 10 caractères.

#### 12. Toutes les chaînes sont-elles numériques ?

Écrivez une fonction qui prend une liste de chaînes de caractères et renvoie `True` si toutes les chaînes sont composées uniquement de chiffres.

#### 13. Chaînes vers entiers

Écrivez une fonction qui prend une liste de chaînes ne contenant que des symboles de chiffres (par exemple `["10", "-3"]` n'est pas demandé ici : uniquement des chiffres 0–9 dans chaque chaîne) et renvoie la liste des entiers correspondants.

#### 14. Nombres pairs uniquement

Écrivez une fonction qui prend une liste d'entiers et renvoie une liste contenant uniquement les nombres pairs, dans le même ordre qu'à l'origine.

#### 15. Mot le plus long

Écrivez une fonction qui prend une liste de mots (non vide) et renvoie le mot le plus long. S'il y a plusieurs mots de longueur maximale, renvoyez celui qui apparaît **en premier** dans la liste.

#### 16. Mots triés par longueur

Écrivez une fonction qui prend une liste de mots et renvoie une **nouvelle** liste contenant les mêmes mots, triés par longueur croissante (du plus court au plus long). En cas de mots de même longueur, conservez l'ordre relatif d'origine.

#### 17. Prénoms et noms

Écrivez une fonction qui prend deux listes de chaînes de même longueur : des prénoms et des noms de famille. Elle renvoie une liste de chaînes du type `"Prénom Nom"` (un espace entre les deux).

#### 18. Total pondéré des notes

Écrivez une fonction qui prend deux listes : une liste de notes et une liste de coefficients. La fonction doit calculer et renvoyer la moyenne pondérée des notes.

#### 19. Indices au-dessus de la moyenne

Écrivez une fonction qui prend une liste de nombres (non vide) et renvoie la liste des **indices** des éléments strictement supérieurs à la moyenne arithmétique de la liste.

#### 20. Écart entre deux nombres

Écrivez une fonction qui prend deux nombres `a` et `b` et renvoie l’écart entre eux sur la droite numérique, c’est-à-dire la distance sans tenir compte duquel est le plus grand.

#### 21. Mot le plus court

Écrivez une fonction qui prend une liste de mots (non vide) et renvoie le mot le plus court. S’il y a plusieurs mots de longueur minimale, renvoyez celui qui apparaît **en premier** dans la liste.

#### 22. Chaîne miroir

Écrivez une fonction qui prend une chaîne de caractères et renvoie une **nouvelle** chaîne dont les caractères sont dans l’ordre inverse (le dernier caractère devient le premier, etc.).

#### 23. Compter les entiers dans un mélange

Écrivez une fonction qui prend une liste dont les éléments peuvent être de types variés (nombres, chaînes, etc.). Elle renvoie le nombre d’éléments qui sont des entiers, **sans** compter les booléens dans ce total.

#### 24. Caractère, code, représentation

Écrivez une fonction qui prend une chaîne `text` et renvoie une liste de triplets (un par caractère, dans l’ordre). Chaque triplet contient : le caractère lui-même ; son code numérique Unicode ; la chaîne que le langage produit pour représenter **ce seul** caractère avec échappement des caractères non ASCII si besoin. Pour chaque position, assurez-vous que l’on retrouve bien le caractère initial à partir de son code numérique.

#### 25. Conversion d'une couleur RGB

Écrivez une fonction qui prend trois nombres entiers (compris entre 0 et 255) et renvoie la chaîne correspondant à la couleur au format hexadécimal `#RRGGBB`. Par exemple, `255, 255, 255` donne `"#FFFFFF"`.

#### 26. Lignes numérotées

Écrivez une fonction qui prend une liste de chaînes (par exemple des lignes de texte) et renvoie une **nouvelle** liste de même longueur : chaque chaîne est précédée de son numéro de ligne et d’un point et d’un espace, en commençant à **1**.  
Exemple : `["Bonjour", "le monde"]` donne `["1. Bonjour", "2. le monde"]`.

#### 27. Somme des carrés

Écrivez une fonction qui prend une liste de nombres et renvoie la somme des carrés de ses éléments (pour une liste vide, la somme vaut `0`).

#### 28. Moyenne arrondie

Écrivez une fonction qui prend une liste de nombres (non vide) et un entier `ndigits`, et renvoie la moyenne arithmétique des éléments, **arrondie** à `ndigits` chiffres après la virgule.

#### 29. Notes arrondies pour affichage

Écrivez une fonction qui prend une liste de nombres (à virgule) et renvoie une **nouvelle** liste : chaque valeur est arrondie à **une** décimale (la liste vide renvoie une liste vide).

#### 30. Liste de présence et notes

Écrivez une fonction qui prend deux listes de même longueur non nulle : des noms (`str`) et des notes (`int` ou `float`). Elle doit renvoyer une liste de chaînes décrivant chaque personne : numéro commençant à **1**, nom, note affichée avec **une** décimale.  
Exemple : noms `["Ada", "Alan"]` et notes `[18.34, 12.0]` donnent des chaînes du type `"1. Ada : 18.3"` et `"2. Alan : 12.0"` (vous choisissez la mise en forme exacte des chaînes, mais la numérotation, le nom et la note arrondie à une décimale doivent apparaître clairement).

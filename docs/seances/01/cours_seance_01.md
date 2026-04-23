---
marp: true
title: "Séance 1 - Introduction à Python"
paginate: true
footer: "[←](../../index.html) · Tech Info 1 - Séance 1"
---

## Séance 1

Introduction à Python

[← Retour à l'accueil](../../index.md)
[→ Exercices](exercices_seance_01.md)
[→ Quiz interactif](quiz_seance_01.html)

---

## Objectifs de la séance

- Comprendre ce qu'est Python (langage + logiciel)
- Installer l'environnement minimal pour exécuter du code
- Écrire et lancer un premier script Python
- Découvrir le REPL et l'IDE Thonny

---

## Python : langage et logiciel

- **Langage de programmation** créé en 1989/1990
- Pensé au départ pour le **scripting** (automatiser des tâches répétitives)
- **Open-source** : gratuit, code source consultable et réutilisable
- **Logiciel** : il faut un interpréteur Python installé sur la machine

---

## Interprété vs compilé

- Python est un **langage interprété**
- À chaque exécution, l'interpréteur lit et exécute les instructions
- À l'inverse, un langage compilé (C/C++) produit d'abord un binaire

**Analogie :**

- Interprété : traduction en direct, phrase par phrase
- Compilé : tout est traduit d'un coup avant la lecture

---

## Conséquences pratiques

- **Avantage** : portabilité (fonctionne sur toute machine avec Python)
- **Inconvénient** : performances souvent inférieures au code compilé
- En pratique : excellent pour apprendre, prototyper, automatiser

---

## Python et la Programmation Orientée Objet

- Python est **orienté objet**
- Un objet représente une entité avec données + comportements
- En Python, « tout est objet » (nombres, chaînes, listes, etc.)

---

## Installer Python

- Site officiel : [python.org/downloads](https://www.python.org/downloads/)
- **Windows** : installer l'exécutable
- **macOS** : Python peut déjà être installé, mais souvent en version ancienne
- **Linux** : Python est généralement déjà installé

---

## Éditeur de texte vs éditeur de code

- Un script Python peut être écrit dans n'importe quel éditeur texte
- Mais un **éditeur de code** apporte :
  - détection du langage
  - coloration syntaxique
  - aide à la saisie
- Exemple d'outils : Notepad++, Kate, Gedit, Geany, VS Code

---

## Pourquoi pas toujours un IDE ?

- Un éditeur de code est souvent :
  - plus léger
  - plus rapide à lancer
  - plus polyvalent pour ouvrir différents types de fichiers
- Un IDE devient utile quand on veut tout faire au même endroit

---

## Premier script Python

Créer un fichier `hello_world.py` avec :

```python
print("hello world")
```

- `print()` affiche un message en sortie
- Une instruction Python correspond souvent à une ligne de code

---

## Exécuter le script

1. Ouvrir un terminal
1. Aller dans le dossier du script :

```bash
cd /chemin/vers/hello_world
```

1. Exécuter :

```bash
python hello_world.py
```

---

## Le REPL (shell interactif)

- Lancer `python` sans fichier dans un terminal
- Le REPL exécute les instructions en direct
- Très utile pour tester rapidement des morceaux de code
- Idéal pour vérifier une idée avant de la mettre dans un fichier

---

## Thonny : IDE Python débutant

- Thonny est un environnement de développement intégré (IDE)
- Permet d'éditer, exécuter et déboguer sans quitter l'outil
- Exercice suggéré : ouvrir `hello_world.py` puis afficher :

```python
print("Goodbye, World.")
```

---

## Variables

Une variable est un **nom** qui référence un objet en mémoire.

- Idée clé : une variable est une **référence**
- Ce n'est pas une "boîte" qui contient directement la valeur
- Une affectation peut changer ce que le nom référence

```python
age = 20
name = "Ada"
temperature = 18.5
```

- Le `=` de l'affectation lie un nom à une valeur
- Choisir des noms explicites améliore la lisibilité
- Une variable peut être réaffectée

---

## Variables : analogie de l'étiquette

Imagine une étiquette collée sur un objet :

- Le nom de variable = l'étiquette (`item`)
- L'objet = la valeur référencée (`"book"`, puis `"pen"`)
- Réaffecter = décoller l'étiquette et la recoller ailleurs

```python
item = "book"
item = "pen"
```

Après la 2e ligne, `item` référence `"pen"` (plus `"book"`).

---

## Commentaires

Les commentaires servent à documenter le code.

```python
# This is a single-line comment
age = 20  # end-of-line comment
```

- Python ignore les commentaires à l'exécution
- Un commentaire explique le **pourquoi**, pas l'évidence

---

## Types numériques

Les trois types de base vus en début de cours :

```python
integer = 42         # int
decimal_number = 3.14  # float
complex_number = 2 + 3j  # complex
```

- `int` : nombres entiers
- `float` : nombres à virgule flottante
- `complex` : nombres complexes (moins fréquent en initiation)

---

## Opérateurs arithmétiques

Dans le REPL, écrivez une opération arithmétique puis appuyez sur Entrée.

```python
2 + 3   # addition
10 - 4  # subtraction
6 * 7   # multiplication
8 / 2   # division
7 // 2  # floor division
7 % 2   # modulo (remainder)
2 ** 3  # power
```

---

## Type booléen

Le type `bool` ne contient que deux valeurs :

```python
True
False
```

- Très utilisé dans les conditions (`if`, `while`)
- Résultat typique d'une comparaison

---

## Opérateurs de comparaison

```python
5 == 5   # equal
5 != 3   # not equal
8 > 2    # strictly greater than
8 >= 8   # greater than or equal
3 < 9    # strictly less than
3 <= 3   # less than or equal
```

Ces expressions renvoient toujours un booléen (`True` ou `False`).

---

## Opérateurs logiques

```python
True and False  # logical AND
True or False   # logical OR
not True        # logical NOT
```

Exemple :

```python
age = 20
is_adult = age >= 18 and age < 130
```

---

## Chaînes de caractères (`str`)

```python
first_name = "Lina"
message = "Hello"
```

- Une `str` est une suite de caractères
- On peut concaténer avec `+`
- On peut obtenir la longueur avec `len(text)`

---

## f-strings

Les f-strings facilitent l'insertion de variables dans du texte :

```python
first_name = "Lina"
age = 20
sentence = f"{first_name} is {age} years old."
print(sentence)
```

- Préfixe `f` devant la chaîne
- Variables/expressions entre accolades `{...}`
- Plus lisible que la concaténation manuelle

---

## Erreurs et messages d'erreur

Quand une instruction est incorrecte, Python affiche une erreur.

```python
2 +
```

- Il faut **lire le message d'erreur** avant de corriger
- Le type d'erreur (`SyntaxError`, `NameError`, etc.) donne une piste
- La ligne indiquée aide à localiser le problème

---

## Conclusion de la séance

- Python : langage interprété, open-source, portable
- Variables, types (`int`, `float`, `bool`, `str`) et opérateurs de base
- Opérateurs de comparaison et logique pour produire des conditions
- Commentaires pour documenter le code
- f-strings pour afficher des messages dynamiques

[→ Quiz interactif](quiz_seance_01.html)

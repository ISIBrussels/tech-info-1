---
marp: true
theme: tech-info
title: "Séance 1 - Introduction à Python"
paginate: true
header: "Tech Info 1 — Séance 1 [Sylvain Huraux - HE2B - ISIB](mailto:shuraux@he2b.be)"
footer: "[Retour à l'accueil](../../index.html)"
---

## Séance 1

Introduction à Python

[→ Quiz](quiz_seance_01.html)
[→ Exercices](exercices_seance_01.html)

---

## Objectifs de la séance

- Comprendre ce qu'est Python (langage + logiciel)
- Écrire et lancer un premier script ; découvrir le REPL et Thonny
- Opérateurs arithmétiques, variables, commentaires
- Types `int`, `float` et `bool`
- Opérateurs de comparaison et logiques
- Type `str` et *f-string*

---

## Python : langage et logiciel

Le terme Python désigne autant un **langage** qu'un **logiciel**.

- Inventé en 1989/90, au départ pour le *scripting*
- Licence *open-source* : gratuit, y compris à des fins commerciales
- Code source consultable et réutilisable
- Pour exécuter du code : installer un **interpréteur** ([python.org/downloads](https://www.python.org/downloads/))

---

## Un langage interprété

À chaque exécution, l'interpréteur traduit les instructions **une par une**.

À l'inverse, un langage compilé (C/C++) analyse d'abord tout le code source.

**Analogie :**

- Interprété : un·e interprète traduit en direct, phrase par phrase
- Compilé : tout est passé dans Translate d'un coup, puis on lit le résultat

---

## Conséquences pratiques

- **Avantage** : la portabilité — le programme tourne sur toute machine où Python est installé
- **Inconvénient** : la performance — une même tâche est en général plus rapide en compilé (typiquement C++)

Python est aussi **orienté objet** : un objet est une entité avec des caractéristiques et des fonctionnalités. En Python, **tout est objet**.

---

## Installer Python

- **Windows** : télécharger l'exécutable et l'installer
- **macOS** : Python est parfois déjà là, souvent trop ancien → installer la version récente
- **Linux** : Python est forcément installé (version selon la distribution)

---

## Éditeur de texte vs éditeur de code

Un script peut s'écrire dans n'importe quel éditeur texte (même le bloc-notes). Un **éditeur de code** apporte :

- détection du langage
- coloration syntaxique
- aide à la frappe

Exemples : Notepad++ (Windows), Xcode (macOS), Kate / Gedit / Geany (Linux).

Plus léger et plus polyvalent qu'un IDE complet — utile pour lire ou modifier un fichier rapidement.

---

## Premier script

Dans l'éditeur, écrire :

```python
print("hello world")
```

- Une **instruction** est une étape du programme (souvent une ligne)
- `print()` est une **fonction** : elle affiche un message en sortie

Enregistrer sous `hello_world.py` (sur Windows, choisir le type `.py`).

---

## Exécuter le script

Ouvrir un terminal (`cmd` / PowerShell, Terminal, Konsole…).

```bash
cd /chemin/vers/le/dossier
python hello_world.py
```

- `cd` : *Change Directory*, changer de dossier courant
- `python hello_world.py` : lancer le script

---

## Le REPL (shell interactif)

Taper `python` sans fichier : Python lance la console interactive (*REPL*).

- Interprète les instructions **en direct**
- Utile pour tester un petit bout de code sans l'écrire « en dur » dans un fichier

---

## Thonny : un IDE

*Thonny* est un *IDE* (*Integrated Development Environment*).

Contrairement à un simple éditeur, on y **édite** et **exécute** le code au même endroit.

Ouvrir `hello_world.py` dans Thonny et le modifier pour afficher `"Goodbye, World."`.

---

## Les opérateurs arithmétiques

Dans le REPL :

```python
4 + 5
```

| symbole | fonctionnalité   |
|---------|------------------|
| `+`     | addition         |
| `-`     | soustraction     |
| `*`     | multiplication   |
| `**`    | puissance        |
| `/`     | division         |
| `//`    | division entière |
| `%`     | modulo           |

L'intérêt réel : **stocker** ces résultats pour les réutiliser.

---

## Les variables

Une variable **contient** une valeur — plus précisément, en Python, elle **référence** un objet.

Rappel : **tout est objet**.

Analogie bibliothèque :

- la **côte** du livre = la variable (elle n'est pas le livre)
- le **livre** = l'objet référencé
- les **étagères** = la RAM

Quand un objet est créé, il est stocké en mémoire. La variable permet de le retrouver.

---

## Affectation

```python
x = 5
```

- `=` n'est **pas** l'égalité mathématique
- il **affecte** l'objet à droite à la variable à gauche
- à gauche du `=` : toujours une variable

**Convention** : *snake_case* (`nb_values`), anglais, pas d'accents.

Dans le REPL, taper `x` affiche ce vers quoi `x` référence.

---

## Réutiliser des variables

```python
y = 10
z = x + y
z
```

`z` « vaut » `15` — plus exactement : `z` référence un objet de type `int` égal à 15.

---

## Les commentaires

Un commentaire commence par `#`. Il est « invisible » pour l'interpréteur.

Pour commenter plusieurs lignes :

```python
"""
print(4 + 5)
print(5 + 10)
print(10 + 50)
"""
```

---

## Les types natifs

Chaque objet a un **type** : ce qu'il *est*. Python fournit des types *built-in*.

| Python | Français |
|--------|----------|
| `int` | entier |
| `float` | nombre à virgule flottante |
| `complex` | complexe |
| `bool` | booléen |
| `str` | chaîne de caractères |
| `list`, `tuple`, `set`, `dict`… | collections (plus tard) |

À partir d'ici : on travaille dans un **script**, plus dans le REPL.

---

## Types numériques et booléen

- `int` : entier, positif ou négatif
- `float` : virgule = **point** (`a = 4.52`)
- `bool` : uniquement `True` ou `False`

Python est un langage **dynamique** :

```python
a = 5
a = 8.55
a = True
```

Une même variable peut successivement référencer un `int`, un `float`, puis un `bool`. Dans d'autres langages, le type est fixé à la déclaration.

---

## Logique booléenne

```python
a, b = True, False
```

**Affectation parallèle** : `a` devient `True`, `b` devient `False`.

L'intérêt principal des booléens : le résultat d'une **comparaison**.

---

## Opérateurs de comparaison

| symbole | signification |
|---------|---------------|
| `<` `>` | strictement inférieur / supérieur |
| `<=` `>=` | inférieur / supérieur ou égal |
| `==` | égal |
| `!=` | différent |
| `x is y` | même objet |
| `x is not y` | objets distincts |

```python
a = 5 < 6
print(a)   # True
```

---

## Opérateurs logiques

| symbole | signification |
|---------|---------------|
| `x or y` | OU |
| `x and y` | ET |
| `not x` | NON |

```python
a = 5 < 6 and 10 < 6
print(a)   # False
```

`and` : les **deux** conditions doivent être vraies. Avec `or`, une seule suffit → `True`.

---

## Chaînes de caractères (`str`)

```python
a_message = "hello world"
another_message = 'hello "friends"'
a_sentence = """I hope you are doing "well"\n me, yes"""
print(another_message + a_sentence)
```

- guillemets, apostrophes ou triples guillemets
- `\n` : saut de ligne ; `\t` : tabulation
- `+` : **concaténation**

---

## Une `str` est une séquence

On accède à un caractère par son **indice** (entre crochets).

```python
first_character = a_message[0]     # h
third_character = a_message[2]     # l
last_character = a_message[-1]     # d
```

**On commence à compter à partir de 0.**

Un indice négatif part de la fin (`-2` = avant-dernier).

---

## Les f-strings

Concaténer un nombre et du texte :

```python
print("You got " + str(english_mark)
      + " in english and " + str(math_mark) + " in maths.")
```

Même résultat, plus lisible (depuis Python 3.6) :

```python
print(f"You got {english_mark} in english and {math_mark} in maths.")
```

Le `f` devant les guillemets active les accolades `{…}` comme emplacements. Sans le `f`, `{` et `}` sont des caractères ordinaires.

---

## Les erreurs

```python
print(4           # Will generate an error
```

```text
SyntaxError: '(' was never closed
```

**Lire le message d'erreur** : type (`SyntaxError`, `NameError`…), fichier, ligne — souvent suffisant pour trouver le problème.

---

## Conclusion de la séance

- Python : langage interprété, open-source, portable ; tout est objet
- Script `.py`, REPL, éditeur de code ou IDE (Thonny)
- Variables = références ; `=` est une affectation
- Types `int`, `float`, `bool`, `str` ; langage dynamique
- Comparaisons et opérateurs logiques → booléens
- `str` : séquence, indices, concaténation, *f-strings*
- Lire les messages d'erreur

[→ Quiz](quiz_seance_01.html)
[→ Exercices](exercices_seance_01.html)

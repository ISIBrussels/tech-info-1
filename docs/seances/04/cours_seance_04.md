---
marp: true
theme: tech-info
title: "Séance 4 — Boucle for et fonctions built-in"
paginate: true
header: "Tech Info 1 — Séance 4 [Sylvain Huraux - HE2B - ISIB](mailto:shuraux@he2b.be)"
footer: "[← Retour à l'accueil](../../index.html)"
---

# Séance 4

Boucle `for` et fonctions *built-in*

[→ Quiz](quiz_seance_04.html)
[→ Exercices](exercices_seance_04.html)

---

## Objectifs de la séance

- Parcourir des collections avec `for` (*for each*)
- `range()`, `enumerate()`, `break` et `continue`
- Connaître les fonctions *built-in* utiles (nombres, itérables, conversions, constructeurs)

---

## `for` en Python : une boucle *for each*

En C, `for` ressemble à un `while` « amélioré ». En Python, `for` **parcourt** un composite (liste, tuple, set…).

Même effet que le `while` de la séance précédente :

```python
for n in range(10):
    print(f"n = {n}")
print("Program exited the for loop")
```

`n` prend successivement les valeurs de `range(10)` : 0 à 9.

---

## Parcourir une liste

```python
languages = ["C", "C++", "Java", "Python", "HTML", "CSS", "PHP", "Go", "Rust"]
for language in languages:
    print(language)
```

`language` vaut `"C"`, puis `"C++"`, … jusqu'à `"Rust"`.

---

## Indice + élément : `enumerate()`

```python
for i, language in enumerate(languages):
    print(f"{i} : {language}")
```

À chaque itération : un tuple `(indice, élément)`. Paramètre optionnel : valeur de départ de l'indice (défaut `0`).

---

## `break` et `continue`

- `break` : **sort** immédiatement de la boucle
- `continue` : passe à l'**itération suivante** (sans finir le corps)

```python
for i in range(5, 500, 5):
    if i == 300:
        break
    if i % 10 == 0:
        continue
    print(i)
```

Les multiples de 10 ne s'affichent pas. Dernier affiché : `295` (`i == 300` → `break`).

---

## Fonctions *built-in*

Élément **inclus de base**, sans module externe. Ex. : `print()`.

Elles évitent de recoder à la main des fonctionnalités déjà fournies.

---

## Fonctions sur les nombres

- `abs(x)` : valeur absolue
- `divmod(x, y)` : tuple `(quotient, reste)` — `//` et `%` combinés
- `pow(x, y)` : `x` puissance `y` (équivalent `**`)
- `round(x)` : arrondi ; `ndigits` optionnel (défaut `0`)

---

## Itérable

Objet qu'on peut **parcourir** avec un `for`. Les collections (donc les séquences) sont des itérables.

---

## Fonctions sur les itérables (1)

- `all(iterable)` : `True` si **tous** les éléments sont `True`
- `any(iterable)` : `True` si **au moins un** est `True`
- `filter(function, iterable)` : éléments `e` pour lesquels `function(e)` est `True`
- `len(iterable)` : nombre d'éléments
- `map(function, iterable)` : applique `function` à chaque élément

---

## Fonctions sur les itérables (2)

- `max` / `min` : plus grande / plus petite valeur
- `reversed` : parcours en ordre inverse
- `sorted` : version **triée** — toujours une `list`, même si l'entrée est un tuple ou un set
- `sum` : somme des éléments
- `zip(it1, it2, …)` : à chaque itération, tuple des éléments de même indice

---

## Conversions numériques (bases)

- `bin(x)` : binaire — `4` → `"0b100"`
- `hex(x)` : hexadécimal — `12` → `"0xC"`
- `oct(x)` : octal — `9` → `"0o10"`

---

## Caractères et Unicode

- `ascii(obj)` : représentation lisible ; caractères non ASCII échappés
- `chr(unicode_value)` : caractère correspondant au code
- `ord(char)` : code Unicode du caractère
- `format(value, form)` : chaîne représentant `value` au format `form`

---

## Constructeurs

Fonction exécutée à l'**instanciation**. Souvent utilisés pour le *casting* :

`bool`, `int`, `float`, `str`, `list`, `tuple`, `set`, `frozenset`, `dict`, `range`, `complex`, `bytes`, `bytearray`, `object`, …

`object` est le type **parent** de tous les autres.

---

## `slice`

```python
numbers = [1, 2, 3, 4.5, 12.5, 10, 20, 34.54, 5.98]
selected_numbers = numbers[slice(2, 8, 2)]
# 3, 12.5 et 20  (stop exclu)
```

Équivalent à `sequence[start:stop:step]`. `start` et `step` optionnels (comme `range`).

---

## Autres fonctions utiles

- `id(obj)` : identifiant unique (`int`) de l'objet
- `isinstance(obj, cls)` : `True` si `obj` est une instance de `cls`
- `type(obj)` : classe dont `obj` est une instance
- `help(obj)` : documentation (très utile dans le REPL, surtout si `obj` est une classe)

---

## Conclusion de la séance

- `for` = *for each* sur un itérable ; `range`, `enumerate`
- `break` sort ; `continue` saute le reste de l'itération
- *Built-in* : nombres (`abs`, `round`…), itérables (`len`, `sum`, `zip`…), bases, Unicode
- Constructeurs = *casting* ; `slice` ≡ `seq[start:stop:step]`

[→ Quiz](quiz_seance_04.html)
[→ Exercices](exercices_seance_04.html)

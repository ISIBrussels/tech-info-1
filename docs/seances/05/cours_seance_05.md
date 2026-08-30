---
marp: true
title: "Séance 5 — Méthodes de str, list et tuple"
paginate: true
footer: "[←](../../index.html) · Tech Info 1 — Séance 5"
---

# Séance 5

Méthodes d'instance de `str`, `list` et `tuple`

[← Retour à l'accueil](../../index.html)
[→ Exercices](exercices_seance_05.html)

---

## Objectifs de la séance

- Distinguer **fonction** et **méthode d'instance** (`obj.methode()`)
- Méthodes de `str` : tests, transformations, recherche / découpage
- Retenir qu'une `str` est **immuable**
- Méthodes de `list` (et celles partagées avec `tuple`)

---

## Méthode d'instance

Fonction définie **dans une classe**, appelée **sur une instance** :

```python
sentence = "hello world"
sentence.upper()    # méthode de la classe str
```

Syntaxe : `variable.instance_method()`.

---

## `str` : méthodes qui testent une condition

Elles renvoient `True` / `False` :

- `endswith` / `startswith`
- `isalnum`, `isalpha`, `isascii`
- `isdecimal`, `isdigit`, `isnumeric`
- `isidentifier`, `islower`, `isupper`, `istitle`
- `isprintable`, `isspace`

**Attention** : `-` et `.` ne sont pas des *digits*. `isdigit` ⊃ les chiffres, pas seulement 0–9 (`²` compte). `isnumeric` est encore plus large (fractions comme `¾`).

---

## `str` : nouvelles chaînes (immuable)

**Un `str` ne se modifie pas.** Ces méthodes **renvoient** une nouvelle chaîne.

- Casse : `upper`, `lower`, `capitalize`, `swapcase`, `title`, `casefold`
- Bords : `strip`, `lstrip`, `rstrip`
- Alignement : `center`, `ljust`, `rjust`, `zfill`
- Autres : `replace`, `expandtabs`, `encode`, `translate`

---

## `join`

Met bout à bout les éléments d'un itérable, séparés par la chaîne sur laquelle on appelle la méthode :

```python
message = " ".join(["these", "are", "words", "from", "a", "sentence"])
print(message)
```

---

## `str` : recherche et découpage

- `count(chars)` : nombre d'occurrences
- `find` / `index` : première occurrence (`-1` vs exception)
- `rfind` / `rindex` : dernière occurrence
- `split` / `rsplit` : découpe → `list` (`separator`, `maxsplit`)
- `splitlines` : découpe sur `\n`
- `partition` / `rpartition` : tuple de 3 (gauche, séparateur, droite)
- `format()` : relativement obsolète depuis les *f-strings*
- `maketrans` + `translate` : table de substitution caractère par caractère

---

## `list` : ajouter

`elements` référence une `list`.

- `append(obj)` : à la fin
- `extend(iterable)` : les éléments d'`iterable` à la fin
- `insert(index, obj)` : à l'indice `index`

---

## `list` : retirer

- `clear()` : vide la liste
- `pop(index)` : retire et **renvoie** l'élément ; sans argument → le dernier
- `remove(obj)` : retire la **première** occurrence de `obj`

---

## `list` : modifier en place

- `reverse()` : inverse l'ordre
- `sort()` : trie la liste

Ces méthodes **modifient** l'objet ; elles ne renvoient pas une nouvelle liste (contrairement à `sorted()`, fonction *built-in*).

---

## `list` et `tuple`

- `copy()` : copie de la liste (**list seulement**)
- `count(obj)` : nombre d'occurrences — **aussi sur `tuple`**
- `index(obj)` : indice de la première occurrence — **aussi sur `tuple`**

Un tuple n'a pas `append`, `sort`, `reverse`… : il est immuable.

---

## Conclusion de la séance

- Méthode = `objet.methode()` ; fonction = `fonction(objet)`
- `str` immuable → les méthodes renvoient une **nouvelle** chaîne
- Tests (`is…`, `startswith`…), transformations, `split` / `join` / `find`
- `list` mutable : `append`, `extend`, `pop`, `sort`, `reverse`
- `tuple` : essentiellement `count` et `index`

[→ Exercices](exercices_seance_05.html)

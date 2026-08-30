---
marp: true
title: "Séance 3 — while, listes, tuples, range"
paginate: true
footer: "[←](../../index.html) · Tech Info 1 — Séance 3"
---

# Séance 3

Boucle `while` et séquences (`list`, `tuple`, `range`)

[← Retour à l'accueil](../../index.html)
[→ Exercices](exercices_seance_03.html)

---

## Objectifs de la séance

- Répéter des instructions avec `while`
- Comprendre les **séquences** (collections ordonnées, indices)
- Manipuler les `list` (mutables) : accès, slicing, modification
- Distinguer `tuple` (immuable) et `range`

---

## La boucle `while`

« Tant que » la condition d'entrée est `True`, on exécute le bloc.

```python
n = 0
while n < 10:
    print(f"n = {n}")
    n += 1  # équivalent à n = n + 1
print("Program exited the while loop")
```

Affiche `n = 0` … `n = 9`, puis le message de sortie.

---

## Déroulement

1. Première arrivée : `n < 10` est `True` (`n` vaut 0) → on entre
2. `n += 1` met à jour `n`
3. Retour au test : encore `True` → nouvelle itération
4. Après 10 itérations, `n` vaut 10 → test `False` → on **sort**
5. On exécute la suite (`print` hors de la boucle)

Sans le `n += 1` : boucle **infinie**.

---

## Les séquences

Types composites **ordonnés** : chaque élément a un **indice**.

Trois types *built-in* : `str`, `list`, `tuple`.

(`str` est déjà une séquence : un caractère = un élément.)

**On commence à compter à partir de 0.**

---

## Le type `list`

Séquence **modifiable** (*mutable*). Crochets `[]` :

```python
mixed_values = [1, 2, 3.5, "hello", True, "red", 3.5, 5.5445, "b"]
```

Une liste peut mélanger les types.

---

## Accès et *slicing*

```python
first_item = mixed_values[0]              # 1er
middle_slice = mixed_values[2:7]          # du 3e au 7e (indice 7 exclu)
from_fifth_item = mixed_values[4:]        # du 5e à la fin
first_five_items = mixed_values[:5]       # des 5 premiers
penultimate_item = mixed_values[-2]       # avant-dernier
items_with_step_two = mixed_values[1:7:2] # pas de 2
```

Borne de fin **exclue**. Indice négatif = depuis la fin.

---

## Modifier une liste

```python
mixed_values[0] = 100
mixed_values[2:5] = [50, 60, 70]
```

Ajouter :

```python
mixed_values.append("important message")  # à la fin
mixed_values.insert(2, "220")             # à l'indice 2
mixed_values.extend(additional_values)    # concaténer une autre liste
```

---

## Méthode vs fonction

`variable.function()` : **méthode d'instance** — elle opère **sur** l'objet.

`append()`, `insert()`, `extend()` travaillent sur `mixed_values`.

`print()` et `input()` sont des **fonctions** : elles s'utilisent « toutes seules ».

---

## Supprimer, longueur, appartenance

```python
mixed_values.remove("important message")
mixed_values.pop(4)      # 5e élément
mixed_values.clear()     # vide la liste

mixed_values_length = len(mixed_values)
is_present = 6 in mixed_values
```

Documentation d'un type dans le REPL : `help(list)`.

---

## Copie vs alias

```python
copied_values = mixed_values.copy()  # nouvelle liste en mémoire
alias_values = mixed_values          # même objet
```

`id()` donne l'identifiant unique d'un objet :

```python
print(id(mixed_values))
print(id(copied_values))   # différent
print(id(alias_values))    # identique à mixed_values
```

---

## Listes multidimensionnelles

Une liste d'objets peut contenir des listes :

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
coefficient = matrix[0][2]   # 3 (ligne 0, colonne 2)
```

---

## Le type `tuple`

Séquence **immuable** (*immutable*). Parenthèses `()` :

```python
sample_tuple = (1, 2, 3, 5, 6.5, "ok", False, "some text")
fourth_item = sample_tuple[3]
```

On **ne peut** ni modifier, ni ajouter, ni retirer d'éléments.

---

## Pourquoi un tuple plutôt qu'une liste ?

- Séquence **protégée** : on veut qu'elle reste constante
- Gain de **performance** (immuable)

Pour des calculs numériques lourds : plutôt `numpy` / `pandas`.

---

## Le type `range`

Séquence d'entiers. Constructeur `range()` :

```python
default_range = range(10)           # 0 à 10 exclu, pas 1
start_stop_range = range(2, 10)     # 2 à 10 exclu
custom_step_range = range(5, 50, 5) # pas de 5
```

On peut construire n'importe quel type ainsi :

```python
values_list = list((1, 2, 5, 10.5, "green"))
values_tuple = tuple([1, 4, 4.5, "ok", "ok"])
integer_value = int(4.0)
```

---

## Conclusion de la séance

- `while` : tant que la condition est `True` ; penser à faire évoluer la condition
- Séquences : `str`, `list`, `tuple` — indices à partir de 0, *slicing*
- `list` : mutable ; méthodes `append` / `insert` / `extend` / `remove` / `pop` / `copy`
- Copie ≠ alias (`id()`)
- `tuple` : immuable ; `range` : suite d'entiers

[→ Exercices](exercices_seance_03.html)

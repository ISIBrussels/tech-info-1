---
marp: true
title: "Séance 2 — Casting, fonctions, conditions"
paginate: true
footer: "[←](../../index.html) · Tech Info 1 — Séance 2"
---

# Séance 2

*Casting*, fonctions, constantes et structures conditionnelles

[← Retour à l'accueil](../../index.html)
[→ Exercices](exercices_seance_02.html)
[→ Quiz interactif](quiz_seance_02.html)

---

## Objectifs de la séance

- Convertir un objet d'un type vers un autre (*casting*)
- Écrire ses propres fonctions (`def`, paramètres, `return`)
- Distinguer variables locales et globales ; instruction `pass`
- Convention des constantes
- Structures `if`, `elif`, `else`

---

## Le *casting* : conversion de type

```python
number = 5
number_in_string = str(number)           # int → str  → "5"
some_string = "4"
integer_from_string = int(some_string)   # str → int
another_string = "5.23"
float_from_string = float(another_string)  # str → float
```

`str()`, `int()` et `float()` **renvoient** un objet : on les place à droite du `=`.

---

## Connaître le type : `type()`

```python
print(number + integer_from_string)
print(type(number))
print(type(some_string))
print(type(float_from_string))
```

---

## *Casting* vers un booléen

```python
bool(1)     # True
bool(0)     # False
bool(-2)    # True
bool(0.5)   # True
bool(0.0)   # False
bool("Hi")  # True
bool("")    # False
bool(" ")   # True
```

- Tout nombre **sauf 0** → `True` (y compris les négatifs)
- Chaîne **vide** → `False` ; dès qu'il y a un caractère (même un espace) → `True`

---

## Les fonctions

Une fonction peut recevoir quelque chose en **entrée** et renvoyer quelque chose en **sortie**.

- `input()` : argument = message à afficher ; renvoie la chaîne saisie
- Une fonction peut n'avoir **aucun** paramètre
- Si elle « ne renvoie rien », elle renvoie en pratique `None`

```python
def print_hello():
    print("hello")
```

---

## `def`, bloc et indentation

- `def` : début de la **définition**
- `:` : début d'un **bloc**
- L'appartenance au bloc = l'**indentation** (touche Tab)

Convention de nommage : *snake_case*, comme les variables.

```python
print_hello()
```

Sans les parenthèses, on ne **l'appelle** pas.

---

## Paramètres, arguments, `return`

```python
def add_two_numbers(a, b):
    return a + b

sum1 = add_two_numbers(2, 4)   # 6
```

- **Paramètre** : nom à la définition (`a`, `b`)
- **Argument** : objet passé à l'appel (`2`, `4`)
- `return` : l'objet renvoyé est référencé par `sum1`

---

## Arguments par défaut et nommés

```python
def power(x, y=2):
    return x ** y

p1 = power(2)        # y = 2 par défaut
p2 = power(4, 4)     # y est écrasé
p3 = power(y=3, x=4) # arguments nommés (ordre libre)
```

---

## Variables locales

Une variable déclarée **dans** la fonction n'existe que pendant l'appel. Ensuite elle est « supprimée ».

Une variable déclarée au niveau du script est **globale** : accessible dans toutes les fonctions.

**Très peu recommandé d'utiliser des variables globales.** On verra plus tard comment s'en passer.

---

## Plusieurs `return`

Dès que l'interpréteur atteint un `return`, la fonction **s'arrête** (même s'il reste du code en dessous).

On peut `return` sans valeur (renvoie `None`).

Intérêt des fonctions : **éviter de répéter** le même bout de code. On compartimente.

---

## L'instruction `pass`

`pass` ne fait **rien**. Un bloc Python **ne peut pas être vide**.

```python
def sort_vegetables():
    pass
```

Utile pour « réserver » le nom d'une fonction dont le corps sera écrit plus tard, sans que le script lève une erreur.

---

## Les constantes

En C++ : `const int myConstant` — réaffecter lève une erreur.

**En Python, il n'y a pas de vraie constante** : aucun mot-clé n'empêche la réaffectation.

Convention : nom **en majuscules** (`DAYS_OF_WEEK`, `ALPHABET_LOWERCASE`) pour indiquer aux autres (et à soi-même) de ne pas modifier cette variable.

---

## `if`

```python
a = 5
if a == 5:
    print("a is equal to 5")
```

- `if` + condition + `:`
- Le bloc indenté ne s'exécute que si la condition vaut `True`
- Une ligne **non indentée** n'appartient pas au `if`

---

## `elif` et `else`

```python
b = 10
if b == 10:
    print("b is 10")
elif b == 15:
    print("b is 15")
else:
    print("b is neither 10 nor 15")
```

- commence toujours par un `if`
- zéro, un ou plusieurs `elif`
- `else` optionnel

---

## L'ordre compte

```python
c = 20
if c > 10:
    print("c is strictly greater than 10")
elif c > 5:
    print("c is strictly greater than 5")
```

Si la première condition est vraie, les suivantes **ne sont pas** évaluées.

Deux `if` indépendants (sans `elif`) : **les deux** blocs peuvent s'exécuter.

---

## Imbrication

```python
d = 12
if d > 5:
    print("d > 5")
    if d > 10:
        print("d > 10")
```

On lit les niveaux grâce à l'indentation.

- `d > 10` → les deux `print`
- `5 < d < 10` → seulement `d > 5`

---

## Conclusion de la séance

- *Casting* : `str()`, `int()`, `float()`, `bool()`, `type()`
- `def` / indentation / paramètres ≠ arguments / `return`
- Variables locales ; `pass` ; constantes = convention MAJUSCULES
- `if` / `elif` / `else` : un seul chemin ; l'ordre des conditions est décisif

[→ Exercices](exercices_seance_02.html)
[→ Quiz interactif](quiz_seance_02.html)

---
marp: true
theme: tech-info
title: "Séance 2 — Casting, conditions, fonctions"
paginate: true
header: "Tech Info 1 — Séance 2 [Sylvain Huraux - HE2B - ISIB](mailto:shuraux@he2b.be)"
footer: "[← Retour à l'accueil](../../index.html)"
---

# Séance 2

*Casting*, structures conditionnelles, fonctions et constantes

[→ Quiz](quiz_seance_02.html)
[→ Exercices](exercices_seance_02.html)

---

## Objectifs de la séance

- Convertir un objet d'un type vers un autre (*casting*)
- Structures `if`, `elif`, `else`
- Écrire ses propres fonctions (`def`, paramètres, `return`)
- Distinguer variables locales et globales ; instruction `pass`
- Convention des constantes

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

## Structures conditionnelles

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
- Dès qu'une branche est vraie, les suivantes **ne sont pas** évaluées

---

## Deux `if` indépendants

Même conditions, même `c = 20` : avec `elif` il y a **dépendance** ; avec deux `if`, **non**.

<style scoped>
.columns {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.2rem;
  align-items: start;
}
.columns pre {
  font-size: 0.72em;
}
</style>

<div class="columns">
<div>

`if` / `elif` : dès qu'une branche est vraie, les suivantes sont **ignorées**.

```python
c = 20
if c > 10:
    print("c > 10")
elif c > 5:
    print("c > 5")
```

→ seulement `c > 10`

</div>
<div>

Deux `if` : **pas** de dépendance — chaque test est évalué.

```python
c = 20
if c > 10:
    print("c > 10")
if c > 5:
    print("c > 5")
```

→ les **deux** `print`

</div>
</div>

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

## Les fonctions

Une fonction peut recevoir quelque chose en **entrée** et renvoyer quelque chose en **sortie**.

**Appeler** une fonction = écrire son **nom** avec les **parenthèses**.

```python
age = int("21")   # prend une entrée, renvoie un objet → on le stocke
print(age)        # prend quelque chose ; « ne renvoie rien » (None) → on ne stocke pas
```

- `int(...)` : convertit et **renvoie** un entier → à droite d'un `=`
- `print(...)` : affiche ; en pratique renvoie `None` → on **ne stocke** pas le retour

```python
print      # sans parenthèses : on n'appelle pas la fonction
print(age) # avec parenthèses : on l'appelle
```

---

## `def`, bloc et indentation

- **Définir** une fonction = lui donner un nom et écrire les instructions qu'elle exécutera à chaque appel
- `def` : début de la **définition**
- `:` : début d'un **bloc**
- L'appartenance au bloc = l'**indentation** (touche Tab)

Convention de nommage : *snake_case*, comme les variables.

```python
def print_hello():
    print("hello")
```

Cet exemple n'a **ni entrée ni sortie** : aucun paramètre, pas de `return`.

---

## Paramètres, arguments, `return`

**Définir** une fonction et **l'appeler**, ce n'est **pas** la même chose : la définition décrit ce qu'elle fait ; l'appel l'exécute.

```python
def discount_price(price, percent):
    factor = 1 - percent / 100
    discounted = price * factor
    return discounted

paid = discount_price(80, 25)   # 60.0
```

- **Paramètre** : nom à la définition (`price`, `percent`)
- **Argument** : objet passé à l'appel (`80`, `25`)
- `return` : l'objet renvoyé est référencé par `paid`

---

## Arguments par défaut et nommés

```python
def repeat_text(text, times=2):
    result = text * times
    return result

r1 = repeat_text("go")                 # times = 2 par défaut
r2 = repeat_text("go", 4)              # times est écrasé
r3 = repeat_text(times=3, text="ok")   # arguments nommés (ordre libre)
```

---

## Variables locales

Une variable déclarée **dans** la fonction n'existe que pendant l'appel. Ensuite elle est « supprimée ».

Une variable déclarée au niveau du script est **globale** : accessible dans toutes les fonctions.

**Très peu recommandé d'utiliser des variables globales.** On verra plus tard comment s'en passer.

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

## Plusieurs `return`

Dès qu'un `return` est atteint, la fonction **s'arrête** (le reste du corps n'est pas exécuté).

```python
def ticket_price(age):
    if age < 12:
        return 5
    elif age < 18:
        return 8
    else:
        return 12

price = ticket_price(15)   # 8
```

Un seul chemin : **un `return` par branche**. On peut aussi `return` sans valeur (renvoie `None`).

---

## Conclusion de la séance

- *Casting* : `str()`, `int()`, `float()`, `bool()`, `type()`
- `if` / `elif` / `else` : un seul chemin ; l'ordre des conditions est décisif
- `def` / indentation / paramètres ≠ arguments / `return`
- Variables locales ; `pass` ; constantes = convention MAJUSCULES

[→ Quiz](quiz_seance_02.html) [→ Exercices](exercices_seance_02.html)

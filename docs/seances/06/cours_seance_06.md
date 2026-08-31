---
marp: true
theme: tech-info
title: "Séance 6 — set, dict, type hinting, main"
paginate: true
header: "Tech Info 1 — Séance 6 [Sylvain Huraux - HE2B - ISIB](mailto:shuraux@he2b.be)"
footer: "[Retour à l'accueil](../../index.html)"
---

# Séance 6

Types `set` et `dict`, *type hinting*, fonction `main()`

[→ Quiz](quiz_seance_06.html)
[→ Exercices](exercices_seance_06.html)

---

## Objectifs de la séance

- Collections non ordonnées : `set` et `frozenset`
- Dictionnaires : paires clef → valeur
- Annoter les types (*type hinting*)
- Structurer un script avec `main()` et `if __name__ == "__main__"`

---

## Le type `set`

Collection **non ordonnée**, longueur variable. Accolades `{}` :

```python
elements = {1, 2, 3, 4, 5, 5, "Hello", 4.5}
```

Pas de doublons : le `5` n'apparaît **qu'une fois**, même écrit deux fois.

Pas d'indexation : `elements[i]` n'existe pas. On ne « modifie » pas un élément par indice, mais on peut **ajouter** ou **retirer**.

---

## `set` : tests entre deux ensembles

- `first.isdisjoint(second)` : aucun élément en commun
- `first.issubset(second)` : tous les éléments de `first` sont dans `second`
- `first.issuperset(second)` : tous les éléments de `second` sont dans `first`

---

## `set` : modifier en place

- `add(obj)` / `discard(obj)` / `remove(obj)` (`remove` lève une erreur si absent)
- `pop()` : retire un élément au hasard
- `clear()` : vide
- `update(second)` : union en place
- `difference_update`, `intersection_update`, `symmetric_difference_update`

Différence : dans `first` mais pas dans `second`. Différence **symétrique** : dans l'un ou l'autre, pas les deux.

---

## `set` : renvoyer un nouvel ensemble

Ne modifient pas les originaux :

- `difference`
- `intersection`
- `symmetric_difference`
- `union`

---

## `frozenset`

Au `set` ce que le `tuple` est à la `list` : **non ordonné** et **immuable**.

```python
fs = frozenset([1, 2, 3, 4])
```

Seul le constructeur permet de le créer.

`set` ↔ `list` comme `frozenset` ↔ `tuple`.

---

## Le type `dict`

Collection **mutable** de paires **clef → valeur** (ordre d'insertion conservé en Python 3.7+).

Analogie du dictionnaire papier : un mot (clef) a une définition (valeur).

```python
d = {
    6: 4.5,
    "size": [4, "flat"],
    75.23: False,
    (1, 2, 3): 10,
}
```

Écrire sur plusieurs lignes : lisibilité (ligne trop longue sinon).

---

## Clefs *hashables*

Les **valeurs** : n'importe quel type.

Les **clefs** : objets *hashables* — en pratique **immuables**. Pas de liste comme clef.

Très souvent des `str`.

---

## Crochets : lire, ajouter, modifier

```python
a = d[6]           # valeur de la clef 6
d[75.23] = 1       # modification (clef déjà présente)
d["hello"] = 55    # création de la paire
```

Si la clef n'existe pas, `d[key]` **lève une erreur**.

---

## `dict` : lire sans planter

- `d.get(key)` : valeur associée ; **pas d'erreur** si la clef manque
- `d.keys()` : itérable des clefs
- `d.values()` : itérable des valeurs
- `d.items()` : itérable de tuples `(clef, valeur)`

---

## `dict` : ajouter / modifier / retirer

- `setdefault(key, default)` : ajoute seulement si la clef est absente ; renvoie toujours la valeur liée à `key`
- `update(pairs)` : souvent un autre dictionnaire
- `pop(key)` : retire la paire
- `popitem()` : retire la **dernière** paire ajoutée
- `clear()` : vide

---

## Copie et `fromkeys`

- `d.copy()` : copie
- `dict.fromkeys(keys, value)` : nouveau dict, mêmes valeur pour toutes les clefs (`value` défaut `None`)

`fromkeys` est un **constructeur** : on l'appelle en général sur la classe `dict`, pas sur une instance (le dict renvoyé ne dépend pas de celle-ci).

---

## *Type hinting*

Annoter les types des paramètres et du retour. Python reste dynamiquement typé : **pas d'erreur à l'exécution** si le type est faux. Sert à la lisibilité et aux vérifications statiques.

```python
def greet(name: str, age: int) -> str:
    return f"Hello {name}, you are {age} years old!"
```

- `name: str` / `age: int` : types attendus
- `-> str` : type renvoyé

---

## Deux parties d'un fichier Python

1. **Définitions** de fonctions
2. Le **programme** qui « fait quelque chose »

Jusqu'ici, le programme était écrit au « niveau zéro » du fichier. En pratique, on le met dans une fonction `main()`.

---

## `main()` et `if __name__ == "__main__"`

```python
def my_function(values, start, stop):
    result = 0
    return result

def main():
    values = [1, 2, 3]
    value = my_function(values, 0, 100)

if __name__ == "__main__":
    main()
```

Le rôle exact de cette condition sera vu plus tard. **À l'examen** : toujours tester dans `main()`, toujours l'appeler dans **exactement** ce `if`.

---

## Conclusion de la séance

- `set` : unique, non indexable ; `frozenset` = version immuable
- `dict` : clefs hashables → valeurs ; `get`, `items`, `update`, `pop`…
- Annotations `: type` et `-> type` : documentation, pas de contrainte runtime
- Script structuré : définitions, puis `main()`, puis `if __name__ == "__main__": main()`

[→ Quiz](quiz_seance_06.html)
[→ Exercices](exercices_seance_06.html)

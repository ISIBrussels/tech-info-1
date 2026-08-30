# Séance 2 — Exercices

[← Retour à l’accueil](../../index.html) · [Slides du cours](cours_seance_02.html)

## Objectif
S’exercer sur : conversion de types, écriture de fonctions et structures conditionnelles (`if` / `elif` / `else`).

## Énoncés

### A. Conversion de types

#### 1. Conversion de types

Écrire un programme qui effectue les conversions suivantes, puis affiche le type et la valeur de chaque résultat :

- `integer_value` en `str` et en `float`
- `integer_text` en `int` et en `float`
- `decimal_text` en `float`

```python
integer_value = 10
integer_text = "20"
decimal_text = "30.5"
```

### B. Fonctions

#### 2. Moyenne de trois notes

Écrivez une fonction qui prend trois nombres `mark1`, `mark2`, `mark3` et retourne leur moyenne (vous pouvez utiliser des parenthèses et la division).

#### 3. Message de bienvenue

Écrivez une fonction qui prend `first_name` et `last_name` et retourne une chaîne comme `Hello, John Doe!`

#### 4. Texte vers entier

Écrivez une fonction qui prend une chaîne `integer_text` représentant un entier, la convertit avec `int()`, puis retourne la valeur obtenue.

#### 5. Périmètre et aire d'un rectangle

Écrivez une fonction qui prend `width` et `height` et retourne le perimètre et l'aire. **NB : `return` peut retourner plusieurs valeurs, si elles sonnt chacune séparées par une virgule**.

#### 6. Minutes vers heures et minutes

Écrivez une fonction qui prend `total_minutes` (entier) et retourne un tuple `(hours, minutes)` correspondant à la même durée (utilisez la division entière `//` et le reste `%`).

#### 7. Hypoténuse

Écrivez une fonction qui prend `side_a` et `side_b`, longueurs des deux côtés droits d'un triangle rectangle, et retourne la longueur de l'hypoténuse sans utiliser `math.sqrt` (pensez à `**`).

#### 8. Distance entre deux points

Écrivez une fonction qui prend `x1`, `y1`, `x2`, `y2` et retourne la distance euclidienne entre les points `(x1, y1)` et `(x2, y2)` (même astuce qu'à l'exercice précédent pour la racine).

#### 9. Prix TTC

Écrivez une fonction qui prend `price_ht` et `vat_rate` (par exemple `0.20` pour 20 %) et retourne le prix TTC avec la formule `price_ht * (1 + vat_rate)`.

### C. Structures conditionnelles

#### 10. Nombre positif, négatif ou zéro

Écrivez une fonction qui prend un nombre en paramètre et affiche `positive`, `negative` ou `zero`.

#### 11. Nombre pair ou impair

Écrivez une fonction qui prend un entier en paramètre et affiche `even` ou `odd`.

#### 12. Trouver le maximum de deux nombres

Écrivez une fonction qui prend deux nombres et affiche le plus grand des deux.

#### 13. Nombre dans un intervalle

Écrivez une fonction qui prend un nombre en paramètre et affiche `True` si ce nombre est compris entre 10 et 20 inclus, sinon `False`.

#### 14. Catégorie d'âge

Écrivez une fonction qui prend un âge entier `age` en paramètre et affiche une catégorie :

- `child` si `age` est inférieur à 12
- `teenager` si `age` est entre 12 et 17 inclus
- `adult` à partir de 18

#### 15. Lettre : voyelle ou consonne

Écrivez une fonction qui prend une lettre (chaîne de longueur 1) et affiche `vowel` ou `consonant`.

#### 16. Divisible par 3 et/ou 5

Écrivez une fonction qui prend un entier et affiche :

- `divisible by 3 and 5`
- `divisible by 3`
- `divisible by 5`
- `not divisible by 3 or 5`

#### 17. Validation de mot de passe (version simple)

Écrivez une fonction qui prend une chaîne `password` et affiche `valid password` si sa longueur est supérieure ou égale à 8, sinon `password too short`.

#### 18. Triangle valide

Écrivez une fonction qui prend trois longueurs `a`, `b`, `c` et affiche `valid triangle` ou `invalid triangle`.  
Rappel : un triangle est valide si `a + b > c`, `a + c > b` et `b + c > a`.

#### 19. Année bissextile

Écrivez une fonction qui prend une année entière `year` et affiche `leap year` ou `not leap year`.  
Rappel : une année est bissextile si elle est divisible par 4, sauf si elle est divisible par 100, sauf si elle est divisible par 400.

#### 20. Mention

Écrivez une fonction qui prend une variable `score` (entre 0 et 20) et affiche :

- `Fail` si `score` est strictement inférieur à 10
- `Pass` si `score` est entre 10 et 13 inclus
- `Good` si `score` est entre 14 et 16 inclus
- `Very good` si `score` est entre 17 et 20 inclus

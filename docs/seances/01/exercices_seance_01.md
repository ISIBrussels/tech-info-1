# Séance 1 — Exercices

[← Retour à l’accueil](../../index.html) · [Slides du cours](cours_seance_01.html)

## A. Calculs numériques

### 1. Calcul de l'âge

Déclarez une variable `birth_year` avec une année de naissance fixe. Calculez l'âge correspondant en 2024 et affichez-le.

### 2. Calcul simple

Déclarez deux variables `a` et `b` avec des valeurs entières. Calculez et affichez leur somme, différence, produit, quotient, et le reste de la division entière.

### 3. Conversion de température

Déclarez une variable `celsius` avec une valeur de température en degrés Celsius. Convertissez-la en degrés Fahrenheit à l'aide de la formule `F=(C×9/5)+32` et affichez le résultat.

### 4. Calcul du périmètre et de l'aire d'un rectangle

Déclarez deux variables `width` et `height` pour la largeur et la hauteur d'un rectangle. Calculez et affichez son périmètre et son aire.

### 5. Calcul de la moyenne

Déclarez trois variables `note1`, `note2`, et `note3` avec des valeurs numériques. Calculez et affichez leur moyenne en utilisant une *f-string* pour un affichage lisible.

### 6. Conversion minutes en heures/minutes

Déclarez une variable `total_minutes` avec une valeur entière. Convertissez cette durée en heures et minutes (exemple : 135 minutes = 2 heures et 15 minutes), puis affichez le résultat.

### 7. Calcul d'un prix TTC

Déclarez une variable `price_ht` (prix hors taxes) et une variable `vat_rate` (taux de TVA, par exemple `0.20` pour 20 %). Calculez le prix TTC et affichez-le.

### 8. Aire et volume d'un pavé droit

Déclarez trois variables `length`, `width` et `height`. Calculez et affichez l'aire totale du pavé droit et son volume.

### 9. Mini facture

Déclarez `quantity`, `unit_price_ht` et `vat_rate`. Calculez puis affichez le sous-total HT, le montant de TVA et le total TTC.

## B. Logique booléenne

### 10. Vérification d'identifiants

Déclarez deux variables `login_ok` et `password_ok` de type booléen. Affichez `True` si la connexion est autorisée (login correct et mot de passe correct), sinon `False`.

### 11. Drapeau rouge

Déclarez deux variables booléennes `is_late` et `has_excuse`. Affichez `True` si l'étudiant est en situation problématique (en retard et sans excuse), sinon `False`.

### 12. Parité d'un nombre

Déclarez une variable `number` avec une valeur entière. Affichez `True` si ce nombre est pair, et `False` s'il est impair.

### 13. Nombre dans un intervalle

Déclarez une variable `value`. Affichez `True` si `value` est compris entre 10 et 20 inclus, sinon `False`.

### 14. Hors intervalle

Déclarez une variable `value`. Affichez `True` si `value` est strictement inférieur à 0 ou strictement supérieur à 100, sinon `False`.

### 15. Validation d'accès

Déclarez deux variables booléennes : `is_student` et `forgot_card`. Affichez `True` si la personne peut entrer dans la bibliothèque (elle doit être étudiante et ne pas avoir oublié sa carte), sinon `False`.

### 16. Année bissextile

Déclarez une variable `year` avec une année entière. Affichez `True` si l'année est bissextile, sinon `False`.
Rappel : une année est bissextile si elle est divisible par 4, sauf si elle est divisible par 100, sauf si elle est divisible par 400.

## C. Chaînes de caractères

### 17. Concaténation de phrases

Déclarez deux variables `phrase1` et `phrase2` contenant chacune une phrase. Affichez la phrase résultante en les concaténant avec un espace entre les deux.

### 18. Affichage des caractères d'une chaîne

Déclarez une variable `word` contenant un mot de 5 caractères exactement. Affichez chaque caractère de ce mot sur une ligne séparée en utilisant les indices.

### 19. Initiales

Déclarez deux variables `first_name` et `last_name`. Affichez les initiales sous la forme `J.D.` (par exemple pour `John Doe`).

### 20. Extraction d'une sous-chaîne

Déclarez une variable `sentence` et affectez-lui une chaine de caractère contenant une phrase d'exactement 10 caractères. Affichez les cinq premiers caractères, puis les cinq derniers, ainsi qu’une partie centrale de trois caractères.

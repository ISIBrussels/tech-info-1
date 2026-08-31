# Séance 5 — Exercices

<nav class="page-nav">
  <a href="../../index.html">← Retour à l'accueil</a>
  <a href="cours_seance_05.html">Slides du cours</a>
</nav>

## A. Chaînes de caractères

### 1. Espaces en bord de chaîne

Écrivez une fonction qui prend une chaîne et renvoie la même chaîne sans espaces (ni tabulations) superflus au début et à la fin.

### 2. Tout en minuscules

Écrivez une fonction qui prend une chaîne et renvoie sa version entièrement en minuscules.

### 3. Préfixe autorisé

Écrivez une fonction qui prend une chaîne `url` et une liste de préfixes autorisés (par exemple `["http://", "https://"]`). Elle renvoie `True` si `url` commence par l’un de ces préfixes (comparaison exacte sur le préfixe).

### 4. Compter les mots

Écrivez une fonction qui prend une phrase (mots séparés par des espaces) et renvoie le nombre de mots. Les espaces multiples ne doivent pas créer de « mots vides ».

### 5. Joindre avec un séparateur

Écrivez une fonction qui prend une liste de chaînes `parts` et une chaîne `separator`. Elle renvoie une seule chaîne : les éléments de `parts` mis bout à bout, séparés par `separator`.

### 6. Lignes non vides

Écrivez une fonction qui prend une chaîne multi-lignes (sauts de ligne `\n`) et renvoie le nombre de lignes qui contiennent au moins un caractère non blanc après suppression des espaces en bout de ligne.

### 7. Uniquement des chiffres

Écrivez une fonction qui prend une chaîne et renvoie `True` si elle est non vide et ne contient que des caractères décimaux au sens de la méthode du langage qui teste les *digits* (`isdigit`), sinon `False`.

### 8. Extension de fichier

Écrivez une fonction qui prend un nom de fichier (chaîne) et une liste d’extensions autorisées (chaînes du type `".pdf"`, `".txt"`). Elle renvoie `True` si le nom de fichier se termine par l’une de ces extensions (comparaison insensible à la casse pour l’extension).

### 9. Zéros à gauche et tabulations

Écrivez deux fonctions (ou une seule avec un paramètre de mode) : l’une qui applique le remplissage par zéros à gauche (`zfill`) à une chaîne numérique et une largeur donnée ; l’autre qui remplace les tabulations par des espaces (`expandtabs`) avec une largeur de tabulation donnée.

### 10. Itinéraire numéroté

Écrivez une fonction qui prend une liste de noms de villes et renvoie une chaîne décrivant l’itinéraire, par exemple `"1. Paris → 2. Lyon → 3. Marseille"`.

### 11. Occurrences d’une sous-chaîne

Écrivez une fonction qui prend deux chaînes `haystack` et `needle`. Elle renvoie un couple (nombre total d’occurrences de `needle` dans `haystack`, indice de la première occurrence, ou `-1` si aucune).

### 12. Dernière occurrence et nom de fichier

Écrivez une fonction qui prend une chaîne `path` et un séparateur `sep` (par exemple `"/"`). Elle renvoie l’indice de la **dernière** occurrence de `sep` (`rfind`, ou `-1`). Écrivez une deuxième fonction (ou la suite du travail) qui, pour le même type de chemin, renvoie uniquement le nom de fichier après le dernier `sep` en utilisant une méthode du type `rpartition`.

### 13. Découper depuis la droite

Écrivez une fonction qui prend une chaîne, un séparateur `sep` et un entier `maxsplit`. Elle renvoie la liste obtenue en découpant avec `sep` en limitant le nombre de découpages en commençant par la **droite** (méthode du type `rsplit` avec `maxsplit`).

### 14. Formatage d'adresse

Écrivez une fonction qui prend une adresse complète sous forme de chaîne (par exemple `" 123 RUE principale , 75000 PARIS "`) et renvoie une version formatée et propre, du type `"123 Rue Principale, 75000 Paris"`.

### 15. Domaine d’une adresse e-mail

Écrivez une fonction qui prend une chaîne représentant un e-mail contenant exactement un caractère `@`. Elle renvoie la partie située à droite du `@` (le domaine), sans espaces en bord.

### 16. Espaces multiples

Écrivez une fonction qui prend une phrase et renvoie une chaîne où toute suite d’espaces consécutifs est réduite à un seul espace, sans espace en début ni en fin.

### 17. Table des matières

Écrivez une fonction qui prend une liste de titres de chapitres et renvoie une table des matières sous forme d’une **seule** chaîne, avec numérotation et alignement obtenu avec des méthodes du type `ljust`, `rjust` ou `center`.

### 18. Chaîne avec emplacements

Écrivez une fonction qui prend un modèle de chaîne utilisant des accolades `{}` pour des emplacements (syntaxe du type `format` sur les chaînes) et suffisamment d’arguments pour les remplir. Elle renvoie la chaîne formatée (sans utiliser de f-string pour cette fois).

### 19. Même texte, casse ignorée

Écrivez une fonction qui prend deux chaînes `a` et `b`. Elle renvoie `True` si elles sont égales après normalisation « insensible à la casse » au sens de la méthode du type `casefold` (appliquée aux deux chaînes avant comparaison).

### 20. Code produit alphanumérique

Écrivez une fonction qui prend une chaîne `code`. Elle renvoie `True` si `code` est non vide et ne contient que des caractères alphanumériques au sens de la méthode `isalnum`, sinon `False`.

### 21. Table de traduction

Écrivez une fonction qui prend une chaîne `text` et deux chaînes `from_chars` et `to_chars` de **même longueur**. Elle construit une table avec la méthode du type `maketrans` puis renvoie la chaîne transformée par `translate`.

### 22. Texte long : fréquence et journal

Écrivez une fonction qui prend une chaîne multi-lignes (plusieurs paragraphes séparés par des sauts de ligne). Elle renvoie : le nombre total de mots dans l’ensemble ; la liste des mots apparaissant au moins trois fois dans tout le texte avec leur nombre d’occurrences (structure de votre choix).

### 23. Lignes CSV et dates

Écrivez une fonction qui prend une liste de chaînes. Chaque chaîne a la forme `"Nom,Prénom,JJ/MM/AAAA"` (trois champs séparés par des virgules). Elle renvoie deux listes : les lignes dont la partie date est une date valide au format `JJ/MM/AAAA` (jours, mois, années dans des plages raisonnables), et les autres ; pour les lignes valides, vous pouvez en plus renvoyer une version nettoyée des champs (espaces, capitalisation).

### 24. Nettoyage de lignes e-mail

Écrivez une fonction qui prend une liste de chaînes au format `"Nom,Prénom,Email"`. Elle renvoie une liste de chaînes reformatées : noms et prénoms mis en forme, champs sans espaces superflus, et exclusion des lignes dont l’e-mail ne contient pas `@`.

### 25. Correction de texte et noms propres

Écrivez une fonction qui prend une chaîne `text` et une liste de noms propres `proper_names`. Elle corrige le texte selon les règles suivantes :

- la première lettre de chaque phrase est en majuscule ;
- les lettres suivantes sont en minuscules, sauf pour les noms propres présents dans `proper_names`.

## B. Listes et tuples

### 26. Premier et dernier

Écrivez une fonction qui prend une liste non vide et renvoie un **tuple** contenant le premier et le dernier élément.

### 27. Copie triée sans modifier l’original

Écrivez une fonction qui prend une liste de nombres et renvoie une **nouvelle** liste contenant les mêmes valeurs triées par ordre croissant, sans modifier la liste passée en argument.

### 28. Première position et nombre d’occurrences

Écrivez une fonction qui prend une liste et une valeur `target`. Elle renvoie un couple `(i, n)` où `i` est l’indice de la **première** occurrence de `target` (méthode `index`) et `n` le nombre total d’occurrences (méthode `count`). Si `target` est absent, vous pouvez lever l’exception du langage pour `index` et renvoyer `(None, 0)` ou une convention explicite que vous documentez.

### 29. Toutes les positions

Écrivez une fonction qui prend une liste et une valeur `target`. Elle renvoie la liste de **tous** les indices où `target` apparaît.

### 30. Trois meilleures notes

Écrivez une fonction qui prend une liste de notes (nombres) et renvoie les trois meilleures valeurs, triées par ordre décroissant (s’il y a moins de trois notes, renvoyer ce qui est disponible).

### 31. Organisation de tâches

Écrivez une fonction qui prend une liste de tâches (chaînes). Elle renvoie une nouvelle liste : éléments distincts, triés par ordre alphabétique.

### 32. Sans doublons, ordre conservé

Écrivez une fonction qui prend une liste et renvoie une nouvelle liste contenant chaque valeur une seule fois, en conservant l’ordre de la **première** apparition.

### 33. Étendre une liste

Écrivez une fonction qui prend une liste `elements` et un itérable `more`. Elle **modifie** `elements` en place en ajoutant à sa fin tous les éléments de `more` un par un (méthode du type `extend`, pas une boucle d’`append` d’une liste entière comme un seul élément).

### 34. Fusion de deux listes de mots

Écrivez une fonction qui prend deux listes de mots. Elle renvoie la liste de tous les mots distincts, triés par ordre alphabétique.

### 35. Union de deux listes sans doublon

Écrivez une fonction qui prend deux listes `first` et `second`. Elle renvoie une liste contenant tous les éléments présents dans l’une ou l’autre, **sans doublon**, en listant d’abord ceux de `first` (dans leur ordre), puis ceux de `second` qui n’étaient pas déjà présents.

### 36. Comparaison de deux classes

Écrivez une fonction qui prend deux listes d’élèves `class_a` et `class_b`. Elle renvoie trois listes : élèves dans les deux listes ; élèves seulement dans `class_a` ; élèves seulement dans `class_b`.

### 37. Notes depuis une liste de couples

Écrivez une fonction qui prend une liste de tuples `(nom, note)` et renvoie la liste des seules notes, dans le même ordre.

### 38. Paires à partir de deux listes

Écrivez une fonction qui prend deux listes `labels` et `values` de **même longueur**. Elle renvoie une liste de tuples `(labels[i], values[i])` pour chaque indice valide.

### 39. Occurrences dans un tuple

Écrivez une fonction qui prend un tuple et une valeur `target`. Elle renvoie le nombre de fois où `target` apparaît dans le tuple (méthode `count` sur le tuple).

### 40. Remplacer un élément dans un tuple

Écrivez une fonction qui prend un tuple, un indice valide et une nouvelle valeur. Elle renvoie un **nouveau** tuple identique au précédent sauf à l’indice donné (sans modifier le tuple d’entrée).

### 41. Insérer dans une liste

Écrivez une fonction qui prend une liste `elements`, un indice `index` et une valeur `value`. Elle **modifie** `elements` en place en insérant `value` à la position `index` (méthode `insert`).

### 42. Inverser en place

Écrivez une fonction qui prend une liste `elements` et **modifie** cette liste sur place pour mettre ses éléments dans l’ordre inverse, sans renvoyer une nouvelle liste (méthode `reverse`). La fonction peut renvoyer `None` ou la même liste pour chaînage, selon votre convention.

### 43. Rotation d’une liste

Écrivez une fonction qui prend une liste non vide et un entier `k` (positif). Elle renvoie une **nouvelle** liste correspondant à une rotation vers la gauche de `k` positions.

### 44. Calcul de panier

Écrivez une fonction qui prend une liste de chaînes du type `"Produit - prix"` (prix numérique parsable). Elle renvoie le prix total, une liste des lignes sans doublons, et une liste des mêmes lignes triées par prix croissant.

### 45. Inventaire avec remise à zéro

Écrivez une fonction qui prend une liste d’inventaire du type `["tomato - 10", "carrot - 2"]`, une action parmi `"add"`, `"remove"`, `"count"` et `"clear"`, et éventuellement un nom de produit selon l’action. Pour `"clear"`, la liste d’inventaire devient vide (méthode du type `clear`). Pour les autres actions, même logique que précédemment (vous fixez le format des lignes).

<nav class="page-nav">
  <a href="../../index.html">← Retour à l'accueil</a>
  <a href="cours_seance_05.html">Slides du cours</a>
</nav>

<footer class="site-footer"><a href="mailto:shuraux@he2b.be">Sylvain Huraux - HE2B - ISIB</a></footer>

# Séance 6 — Exercices

<nav class="page-nav">
  <a href="../../index.html">← Retour à l'accueil</a>
  <a href="cours_seance_06.html">Slides du cours</a>
</nav>

## A. Ensembles (`set`)

### 1. Filtrage des doublons

Écrivez une fonction `remove_duplicates(items: list)` qui prend une liste d’éléments et renvoie une liste sans doublons (pas besoin de conserver l'ordre initial des éléments).

### 2. Vérification de disponibilité

Écrivez une fonction `check_availability(stock: set, items: list)` qui prend un ensemble représentant les produits disponibles en stock et une liste d’articles demandés. La fonction renvoie les articles disponibles et ceux qui sont indisponibles (structure de votre choix : deux listes, deux ensembles, un dictionnaire, etc.).

### 3. Liste d’invités communs

Écrivez une fonction `find_common_guests(event1: set, event2: set)` qui prend deux ensembles de noms d’invités pour deux événements et renvoie l’ensemble des invités présents aux **deux** événements.

### 4. Catégories uniques

Écrivez une fonction `unique_categories(categories: list)` qui prend une liste de catégories (chaînes, éventuellement répétées) et renvoie un ensemble contenant toutes les catégories distinctes.

### 5. Comparaison de deux ensembles

Écrivez une fonction `compare_sets(left: set, right: set)` qui prend deux ensembles et renvoie :

- les éléments présents uniquement dans `left` ;
- ceux présents uniquement dans `right` ;
- ceux communs aux deux.

### 6. Union de plusieurs listes

Écrivez une fonction `union_of_lists(nested: list)` qui prend une liste dont chaque élément est une liste (ou un itérable) et renvoie l’**ensemble** de toutes les valeurs apparaissant au moins une fois dans l’une de ces listes.

### 7. Sous-ensemble

Écrivez une fonction `is_subset(candidate: set, container: set)` qui renvoie `True` si tout élément de `candidate` est aussi dans `container`, sinon `False`. Utilisez la méthode d’ensemble prévue à cet effet (`issubset` ou équivalent).

### 8. Ensembles disjoints

Écrivez une fonction `are_disjoint(left: set, right: set)` qui renvoie `True` si `left` et `right` n’ont aucun élément en commun, sinon `False`.

### 9. Différence symétrique (sans modifier les originaux)

Écrivez une fonction `symmetric_difference_sets(left: set, right: set)` qui renvoie un **nouvel** ensemble contenant les éléments qui sont dans `left` ou dans `right`, mais pas dans les deux à la fois. Ni `left` ni `right` ne doivent être modifiés.

### 10. Invités sur plusieurs événements

Écrivez une fonction `guest_stats(events: list)` qui prend une liste non vide d’ensembles de noms (un ensemble par événement). Elle renvoie un couple `(present_everywhere, present_at_least_once)` : le premier ensemble contient les noms présents dans **tous** les événements, le second la **réunion** de tous les invités (au moins un événement).

## B. Dictionnaires (`dict`)

### 11. Liste vers dictionnaire

Écrivez une fonction `list_to_dict(keys: list, values: list)` qui prend deux listes de **même longueur** (clefs et valeurs) et renvoie le dictionnaire correspondant.

### 12. Occurrences de mots

Écrivez une fonction `word_count(text: str)` qui prend une chaîne et renvoie un dictionnaire dont les clefs sont les mots et les valeurs le nombre d’occurrences de chaque mot.

### 13. Gestion d’un inventaire

Écrivez une fonction `update_inventory(inventory: dict, action: str, item: str, quantity: int = 0)` qui prend un dictionnaire d’inventaire (produit → quantité), une action parmi `"add"`, `"remove"` et `"update"`, un nom de produit et une quantité optionnelle. La fonction met à jour l’inventaire en place selon l’action.

### 14. Fusion de commandes

Écrivez une fonction `merge_orders(orders1: dict, orders2: dict)` qui prend deux dictionnaires (produit → quantité commandée) et renvoie un dictionnaire fusionné en **additionnant** les quantités pour les produits communs.

### 15. Article le plus vendu

Écrivez une fonction `find_top_item(sales: dict)` qui prend un dictionnaire (article → quantité vendue) et renvoie l’article le plus vendu (en cas d’égalité, indiquez la convention que vous adoptez).

### 16. Moyennes par élève

Écrivez une fonction `calculate_averages(grades: dict)` qui prend un dictionnaire (élève → liste de notes) et renvoie un nouveau dictionnaire associant chaque élève à sa moyenne arithmétique.

### 17. Catalogue filtré par prix

Écrivez une fonction `filter_catalog(catalog: dict, price_limit: float)` qui prend un catalogue (produit → prix) et renvoie un dictionnaire ne contenant que les produits dont le prix est inférieur ou égal à `price_limit`.

### 18. Fusion de carnets d’adresses

Écrivez une fonction `merge_contacts(contacts1: dict, contacts2: dict)` qui fusionne deux dictionnaires (nom → numéro). En cas de nom présent dans les deux carnets, le numéro issu de `contacts2` l’emporte.

### 19. Tri par valeurs

Écrivez une fonction `sort_by_values(data: dict)` qui prend un dictionnaire et renvoie une **liste de tuples** `(clef, valeur)` triée par valeur croissante.

### 20. Suivi des connexions

Écrivez une fonction `track_access(logs: dict, user: str)` qui prend un dictionnaire (utilisateur → nombre de connexions) et un nom d’utilisateur. Elle incrémente le compteur de cet utilisateur (création à `1` s’il était absent) et renvoie le dictionnaire mis à jour.

### 21. Fréquences avec `get`

Écrivez une fonction `tally(items: list)` qui prend une liste d’éléments *hashables* et renvoie un dictionnaire (élément → nombre d’occurrences). Construisez le résultat en utilisant **`dict.get`** (pas `Counter`).

### 22. Filtrer par préfixe de clef

Écrivez une fonction `keys_starting_with(data: dict, prefix: str)` qui prend un dictionnaire dont les clefs sont des chaînes et renvoie un **nouveau** dictionnaire ne contenant que les paires dont la clef commence par `prefix`.

### 23. Inverser le dictionnaire

Écrivez une fonction `invert_mapping(original: dict)` qui prend un dictionnaire dont les **valeurs sont hashables** (pour pouvoir servir de clefs). Elle renvoie un nouveau dictionnaire où chaque valeur de `original` devient une clef ; la valeur associée est la **liste** de toutes les clefs de `original` ayant cette valeur (ordre libre dans chaque liste).

### 24. Notes au-dessus d’un seuil

Écrivez une fonction `scores_above(scores: dict, threshold: float)` qui prend un dictionnaire (nom → note numérique) et un seuil. Elle renvoie un nouveau dictionnaire avec uniquement les entrées dont la note est **strictement supérieure** à `threshold`.

### 25. Initialisation avec `setdefault`

Écrivez une fonction `append_to_groups(groups: dict, key: str, value)` où `groups` associe une clef de groupe à une **liste**. La fonction ajoute `value` à la liste du groupe `key`. Si la clef n’existe pas encore, la liste doit être créée. Utilisez **`setdefault`** sur le dictionnaire pour gérer la création de liste.

### 26. Mise à jour en place

Écrivez une fonction `apply_patch(base: dict, patch: dict)` qui met à jour `base` **en place** avec les paires de `patch` (comme `update`), puis renvoie `base` (le même objet).

### 27. Retrait avec valeur par défaut

Écrivez une fonction `pop_or_default(mapping: dict, key, default)` qui retire `key` de `mapping` et renvoie la valeur associée si elle existait ; si la clef est absente, ne modifie pas le dictionnaire et renvoie `default`. Utilisez la méthode **`pop`** avec sa forme à deux arguments.

### 28. Grille de scores à zéro

Écrivez une fonction `zero_scores(players: list)` qui prend une liste de noms de joueurs et renvoie un nouveau dictionnaire associant chaque joueur au nombre `0`, en vous aidant de **`dict.fromkeys`** (ou en documentant l’équivalent).

### 29. Fusionner des compteurs

Écrivez une fonction `merge_counts(dicts: list)` qui prend une liste de dictionnaires (clef → entier positif ou nul). Elle renvoie un **nouveau** dictionnaire : pour chaque clef apparue dans au moins un des dictionnaires, la valeur est la **somme** des entiers correspondants.

### 30. Classement par score

Écrivez une fonction `rank_by_score(scores: dict)` qui prend un dictionnaire (participant → score numérique) et renvoie une **liste de noms** triée par score **décroissant**. En cas d’égalité de score, ordonnez les noms par ordre **alphabétique** croissant.

<nav class="page-nav">
  <a href="../../index.html">← Retour à l'accueil</a>
  <a href="cours_seance_06.html">Slides du cours</a>
</nav>

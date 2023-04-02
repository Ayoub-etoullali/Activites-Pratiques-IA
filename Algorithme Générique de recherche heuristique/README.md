# Algorithme Générique de recherche heuristique

L'algorithme générique de recherche heuristique dans un graphe est appelé "A* search" (prononcé "A-star search" en anglais). Il s'agit d'un algorithme de recherche de chemin qui utilise une heuristique pour guider la recherche vers la solution la plus proche de l'objectif.

L'algorithme A* utilise une fonction d'évaluation qui combine le coût du chemin actuel à partir du nœud de départ avec une estimation du coût du chemin restant vers l'objectif. Cette fonction d'évaluation est appelée la fonction f(n) et est définie comme suit :

f(n) = g(n) + h(n)

où :

g(n) est le coût du chemin actuel à partir du nœud de départ jusqu'au nœud n.
h(n) est une estimation du coût du chemin restant de n au nœud objectif.
La fonction h(n) est une heuristique, c'est-à-dire une estimation de la distance réelle entre n et l'objectif. Cette heuristique peut être admissible (c'est-à-dire qu'elle ne surestime jamais le coût) ou non admissible.

L'algorithme A* explore le graphe en évaluant tous les nœuds accessibles depuis le nœud de départ en fonction de leur fonction f(n), et en choisissant le nœud avec la fonction f(n) la plus faible. L'algorithme s'arrête lorsque le nœud objectif est atteint ou lorsque tous les nœuds ont été évalués sans trouver de solution.

L'algorithme A* est largement utilisé dans les jeux vidéo, les systèmes de navigation, la robotique et d'autres applications qui nécessitent une recherche de chemin efficace dans des graphes de grande taille.
***

### Voici l'algorithme de recherche A* pour trouver le chemin le plus court dans un graphe :
  #### Entrées :

  - nœud de départ "start"
  - nœud objectif "goal"
  - graphe avec des nœuds connectés par des arêtes
  - une fonction heuristique h(n) qui estime le coût du chemin restant de n au nœud objectif
  
  #### Sortie : le chemin le plus court de start à goal

  1. Initialiser les structures de données :

   - une liste ouverte pour les nœuds à explorer (initialement contient seulement start avec f = g(start) + h(start))
   - une liste fermée pour les nœuds déjà évalués (initialement vide)
   - un dictionnaire pour stocker les coûts g(n) de chaque nœud (initialement contient seulement start avec g(start) = 0)
  
  2. Tant que la liste ouverte n'est pas vide :

   - sélectionner le nœud avec le plus petit coût f(n)
   - si ce nœud est le goal, alors retourner le chemin
   - sinon, pour chaque nœud voisin m du nœud sélectionné :
      * calculer le nouveau coût g(m) en ajoutant le coût de l'arête de n à m au coût g(n) de n
      * si m n'est pas déjà dans la liste ouverte ou fermée, alors :
            - calculer le coût f(m) = g(m) + h(m)
            - ajouter m à la liste ouverte avec le coût f(m)
            - stocker le coût g(m) dans le dictionnaire
      * sinon, si le nouveau coût g(m) est inférieur au coût g(m) actuel, alors mettre à jour la liste ouverte avec le nouveau coût f(m) et mettre à jour le coût g(m) dans le dictionnaire
   - Si la liste ouverte est vide et que le goal n'a pas été trouvé, alors il n'y a pas de solution.

### Voici un exemple d'implémentation en Python :

![Algorithme Générique](https://github.com/Ayoub-etoullali/Activites-Pratiques IA/edit/main/Algorithme%20G%C3%A9n%C3%A9rique%20de%20recherche%20heuristique/Algorithme Générique)

```

```

<kbd>Enjoy Code</kbd> 👨‍💻

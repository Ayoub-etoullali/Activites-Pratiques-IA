# (4) Spring MVC JPA Hibernate Spring Data Thymeleaf

`Exercice :` <br>
1) Donner une écriture récursive de l'algorithme de recherche en profondeur limitée 
2) En déduire alors une écriture de l'algorithme de recherche en profondeur itérative
   ***

### Question 1 :
L'algorithme de recherche en profondeur limitée peut s'écrire de manière récursive de la manière suivante :
![DLS-Algorithm](https://user-images.githubusercontent.com/92756846/226997831-e1d44987-adff-4819-b63a-d2a364ba59f0.jpg) <br>

L'algorithme de recherche en profondeur itérative peut s'écrire en utilisant une boucle qui augmente progressivement la profondeur limite :
![IDS-Algorithm](https://user-images.githubusercontent.com/92756846/226997960-759044cb-299a-48e0-aafa-49d06ea9c0c0.jpg) <br>

L'algorithme de recherche en profondeur itérative effectue des recherches de plus en plus profondes jusqu'à ce qu'une solution soit trouvée ou que la profondeur maximale soit atteinte. À chaque itération, il utilise l'algorithme de recherche en profondeur limitée pour effectuer une recherche en profondeur jusqu'à la profondeur maximale autorisée. Si une solution est trouvée, l'algorithme renvoie le succès. Sinon, il augmente la profondeur maximale et recommence la recherche.

La fonction recherche_profondeur_limitee correspond à l'algorithme de recherche en profondeur limitée, tandis que la fonction recherche_profondeur_iterative correspond à l'algorithme de recherche en profondeur itérative qui utilise la fonction recherche_profondeur_limitee.

Notez que pour la profondeur maximale, nous avons utilisé une valeur arbitrairement grande, représentée par float('inf'). Vous pouvez la remplacer par une valeur appropriée pour votre problème.

```
class ProblemeGraphe:
    def __init__(self, graphe, depart, arrivee):
        self.graphe = graphe
        self.depart = depart
        self.arrivee = arrivee
    
    def est_but(self, noeud):
        return noeud == self.arrivee
    
    def successeurs(self, noeud):
        return self.graphe[noeud]
```

Dans cet exemple, le graphe est représenté par un dictionnaire dont les clés sont les nœuds et les valeurs sont les listes de successeurs de chaque nœud. Le problème consiste à trouver le chemin le plus court de depart à arrivee dans ce graphe.

L'algorithme de recherche en profondeur itérative est utilisé pour trouver ce chemin, en utilisant la classe ProblemeGraphe pour représenter le problème.

<kbd>Enjoy Code</kbd> 👨‍💻

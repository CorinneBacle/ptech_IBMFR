# Dashboard & NodeRed

Commençons par examiner les nœuds node-red-dashboard et d’obtenir une configuration simple de tableau de bord.

Pour commencer, connectons un simple flux qui envoie un nombre aléatoire entre 0 et 99 à un graphique simple. 
Pour cela, vous aurez besoin d’un **nœud d’injection** qui se déclenche de manière répétée toutes les quelques secondes, d’un nœud de fonction pour générer le nombre aléatoire et l’un des nœuds graphique du tableau de bord.

Avant de regarder le fonctionnement du nœud de graphique, configurons le nœud d’injection pour qu’il envoie un horodatage toutes les 5 secondes en définissant la charge utile sur horodatage et sur le champ de répétition sur un intervalle de 5 secondes.

Cela agira comme notre déclencheur à répétition. Nous devons maintenant configurer le noeud de fonction pour générer un nombre aléatoire. Pour ce faire, nous utiliserons une simple fonction mathématique JS:

```msg.payload = Math.round(Math.random()*100);
return msg;
```
Avant de regarder le fonctionnement du nœud de graphique, configurons le nœud d’injection pour qu’il envoie un horodatage toutes les 5 secondes en définissant la charge utile sur horodatage et sur le champ de répétition sur un intervalle de 5 secondes.


Cela générera un nombre aléatoire compris entre 0 et 99 qui sera transmis au nœud de graphique.

Voyons maintenant le noeud **Graphique**. Lorsque vous double-cliquez dessus, vous verrez ses options de configuration:



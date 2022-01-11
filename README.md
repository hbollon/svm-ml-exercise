# Support Vector Machine

Dans notre exemple, nous allons observer l'admission d'étudiants vers l'année supérieure et leurs notes d'examens.

Chaque étudiant à passé deux examens et a donc 2 notes. Certains on réussi à passer, d'autres non. Ces étudiants sont séparés dans deux régions différentes.
On voit bien que l'on peut séparer les données en deux ensembles distincts :

![output1](https://github.com/hbollon/svm-ml-exercise/blob/main/images/output.png?raw=true)

Cependant, la frontière entre ces deux régions n’est pas connue. Ce que l’on veut, c’est que lorsque l'on présentera un nouvel éleve ayant passé ses examens dans un autre établissement et dont on ne connaît que la position dans le plan, l’algorithme de classification sera capable de prédire si ce nouvel éleve va passer ou non.

Le SVM est une solution à ce problème de classification. Le SVM appartient à la catégorie des classificateurs linéaires (qui utilisent une séparation linéaire des données), et qui dispose de sa méthode à lui pour trouver la frontière entre les catégories.

Pour que le SVM puisse trouver cette frontière, il est nécessaire de lui donner des données d’entraînement. En l’occurrence, on donne au SVM un ensemble de points, dont on sait déjà si ce sont des bons éléves ou non. À partir de ces données, le SVM va estimer l’emplacement le plus plausible de la frontière: c’est la période d'entraînement, nécessaire à tout algorithme d’apprentissage automatique.

Une fois la phase d’entraînement terminée, le SVM a ainsi trouvé, à partir de données d’entraînement, l’emplacement supposé de la frontière.

![output1](https://github.com/hbollon/svm-ml-exercise/blob/main/images/output1.png?raw=true)

Il existe plusieurs lignes droites qui peuvent séparer nos catégories. La plupart du temps, il y en a une infinité… Alors, laquelle choisir?

![output2](https://github.com/hbollon/svm-ml-exercise/blob/main/images/output2.png?raw=true)

Intuitivement, on se dit que si on nous donne un nouveau point, très proche des ronds rouges, alors ce point a de fortes chances d’être un rond rouge lui aussi. Inversement, plus un point est près des points verts, plus il a de chances d’être lui-même un point vert. Pour cette raison, un SVM va placer la frontière aussi loin que possible des points verts, mais également aussi loin que possible des points rouges.
On dit de cette frontière qu’elle a la meilleure capacité de généralisation. Ainsi, le but d’un SVM est de trouver cette frontière optimale, en maximisant la distance entre les points d’entraînement et la frontière.

Les points d’entraînement les plus proches de la frontière sont appelés vecteurs support et c’est d’eux que les SVM tirent leur nom: SVM signifie Support Vector Machine, ou Machines à Vecteur Support en français. Dit "Support", car ce sont ces points qui «supportent» la frontière.

<br><br>

Dans certains cas, il est impossible de trouver de ligne droite qui soit une frontière: on dit que les données d’entraînement ne sont pas linéairement séparables:

![output3](https://github.com/hbollon/svm-ml-exercise/blob/main/images/output3.png?raw=true)

Dans ce genre cas on peut utiliser ce qu'on appele un `kernel trick`: Je vous laisse aller voir par vous-même [sur cette rubrique par exemple](https://fr.wikipedia.org/wiki/Machine_%C3%A0_vecteurs_de_support#Cas_non_s%C3%A9parable_:_kernel_trick).

<br><br><br><br>

[Vous pouvez récupérer le fichier CSV ainsi que le fichier Jupyter à compléter ici](https://github.com/hbollon/svm-ml-exercise).

(N'hésitez pas à star le projet et à devenir sponsor pour soutenir les petits développeurs locaux)

[Vous pouvez maintenant faire l'exercice en cliquant sur ce lien](https://guarded-ridge-06310.herokuapp.com/eudpquhe).

---
jupytext:
  encoding: '# -*- coding: utf-8 -*-'
  formats: ipynb,md:myst
  split_at_heading: true
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

Le but de cette séance est de reprendre les expériences précédentes en chercher à faire un bilan des sources d'incertitude puis quantifier les incertitudes-type associés. Vous devrez utiliser ce bilan pour obtenir l'incertitude sur $f'$ pour chaque méthode. Vous terminerez par deux études pour conclure :
* comparer les différentes méthodes entre elle en terme de précision et en terme de cohérence.
* comparer les différentes méthodes avec la valeur constructeur.
* faire la moyenne des valeurs obtenues et en déduire une valeur de $f'$ et comparer cette valeur avec la valeur constructeur.

La page ci-présente existe en version notebook téléchargeable grâce au bouton ![Bouton](./images/bouton_tl.png) (choisir le format `.ipynb`). On rappelle qu'l faut ensuite l'enregistrer dans un répertoire adéquat sur votre ordinateur (`tp2` par exemple dans votre répertoire personnel) puis lancer Jupyter Notebook depuis Anaconda pour accéder au notebook, le modifier et exécutez les cellules de code adéquates.

+++

# (TP) Etude quantitative

+++

## Méthode de Descartes. (1h30)

### Réalisation des mesure avec bilans d'incertitude.

Maintenant que vous avez fait une première fois les mesures pour la méthode de Descartes, vous pouvez réfléchir aux sources d'incertitudes qui ont limité la précision de votre mesure. Refaire la manipulation en cherchant à le bilan des sources d'incertitude et estimer l'incertitude-type pour chaque source. Vous rendrez compte sur votre compte-rendu des sources __pour chaque mesurande directe.__

+++

### Traitement des résultats avec Python.
Remplissez la cellule de code ci-après pour propager l'incertitude à la distance focale $f'$. On considérera pour simplifier que __toutes les distributions statistiques associées aux différentes lois sont uniformes__.


```{code-cell} ipython3
:tags: [remove-output]
"""
On importe pour vous les bibliothèques scientifiques utiles.
"""
import numpy as np
import numpy.random as rd
import matplotlib.pyplot as plt


"""
Commencer par entrer les résultats de mesurage pour les trois mesurandes directes
"""
x1_mes = 0  # Commentaire à remplacer par la descritpion de x1
x2_mes = 0  # Commentaire à remplacer par la descritpion de x2
x3_mes = 0  # Commentaire à remplacer par la descritpion de x3


"""
Pour chaque source d'incertitude créer une ligne ou vous entrez la valeur de de la demi-largeur de la distribution uniforme.
"""
# Sources d'incertitudes pour x1
x1_d1 = 0  # Décrire ici la source d'incertitude associée
x1_d2 = 0  # Décrire ici la source d'incertitude associée

# Sources d'incertitudes pour x2



# Sources d'incertitudes pour x3



"""
Créer les échantillons pour chaque source d'incertitude.
On rappelle que pour un tirage de N valeurs suivant une loi uniforme centrée en 0 et de demi-largeur dt, la fonction est 
rd.uniform(-dt, dt, N)
"""
N = 100000
x1_d1_sim = rd.uniform(-x1_d1, x1_d1, N)
x1_d2_sim = rd.uniform(-x1_d2, x1_d2, N)


"""
Créer à partir des échantillons précédents, les échantillons simulés des mesurandes x1, x2, x3
(ne pas oublier le résultat de mesurage).

Créer ensuite les échantillons simulés de OA, OA' puis f'.
"""
x1_sim = 0
x2_sim = 0
x3_sim = 0
OA_sim = 0
OA1_sim = 0
f1_sim = 0

"""
On affiche pour vous les résultats pour chaque grandeur
"""
print("Résultat de mesurage pour x1 (sans unités) : " + str(np.mean(x1_sim)))
print("Résultat de mesurage pour u(x1) (sans unités) : " + str(np.std(x1_sim, ddof=1)))

print("Résultat de mesurage pour x2 (sans unités) : " + str(np.mean(x2_sim)))
print("Résultat de mesurage pour u(x2) (sans unités) : " + str(np.std(x2_sim, ddof=1)))

print("Résultat de mesurage pour x3 (sans unités) : " + str(np.mean(x3_sim)))
print("Résultat de mesurage pour u(x3) (sans unités) : " + str(np.std(x3_sim, ddof=1)))

print("Résultat de mesurage pour OA (sans unités) : " + str(np.mean(OA_sim)))
print("Résultat de mesurage pour u(OA) (sans unités) : " + str(np.std(OA_sim, ddof=1)))

print("Résultat de mesurage pour OA1 (sans unités) : " + str(np.mean(OA1_sim)))
print("Résultat de mesurage pour u(OA1) (sans unités) : " + str(np.std(OA1_sim, ddof=1)))


"""
Représenter graphiquement l'histogramme des valeurs simulées.
On donne le squelette pour le tracé du graphique. Ajouter/modifier les instructions.
"""
f, ax = plt.subplots()
f.suptitle("Simulation de Monte-Carlo pour f'")
ax.set_xlabel("")  # Ajouter une légende aux abscisses (grandeur et unité)

# Mettre ici l'instruction traçant l'histogramme des valeurs.

plt.show()

"""
Calculer et afficher le résultat de mesurage de f' et son incertitude-type.
"""

f1 = 0  # Entrer la formule adéquate pour le calcul de f'
f1_u = 0  # Entrer la formule adéquate pour le calcul de l'incertitude sur f'

print("Résultat de mesurage : " + str(f1))
print("Incertitude-type : " + str(f1_u))
```

+++

### Compte-rendu des résultats.
Dans votre compte-rendu écrit, vous devez maintenant rendre compte des grandeurs suivantes avec leurs incertitudes : $x_1, x_2, x_3, OA, OA', f'$.

__Pensez bien à la cohérence des chiffres significatifs. On rappelle qu'on ne gardera que deux chiffres significatifs pour les incertitudes de mesure.__

+++

### Exploitation des résultats avec Python
Vous devez maintenant comparer le résultat de mesure à la valeur constructeur. Lire la valeur sur la lentille utilisée.

__Le constructeur annonce une précision de 10% sur la valeur de la focale.__ Sans plus de précision, on considérera qu'il s'agit de l'incertitude-type.

Utiliser la cellule ci-dessous pour calculer et afficher l'écart normalisé. Vous rendrez compte sur votre copie du résultat trouvé et commenterez la cohérence entre votre résultat d'expérience et le valeur constructeur.

```{code-cell} ipython3
:tags: [remove-output]
"""
On rappelle que les variables enregistrées à la cellule précédente sont encore en mémoire.

Commencer par entre les valeurs constructeurs.
"""
f1_c = 0  # Valeur constructeur
f1_cu = 0  # Incertitude constructeur

f1_en = 0  # Ecart normalisé

print("Ecart normalisé : " + str(f1_en))
```

+++

## Méthode de Bessel. (1h30)

### Réalisation des mesure avec bilans d'incertitude.

Maintenant que vous avez fait une première fois les mesures pour la méthode de Bessel, vous pouvez réfléchir aux sources d'incertitudes qui ont limité la précision de votre mesure. Refaire la manipulation en cherchant à le bilan des sources d'incertitude et estimer l'incertitude-type pour chaque source. Vous rendrez compte sur votre compte-rendu des sources __pour chaque mesurande directe.__

+++

### Traitement des résultats avec Python.
Remplissez la cellule de code ci-après pour propager l'incertitude à la distance focale $f'$. On considérera pour simplifier que __toutes les distributions statistiques associées aux différentes lois sont gaussiennes__.

Utilisez les cellules précédentes pour écrire votre code.  __Ne pas utiliser des noms de variables déjà utilisé pour ne pas effacer les résultats précédents__.


```{code-cell} ipython3
:tags: [remove-output]
"""
Les bibliothèques scientifiques utiles ont déjà été importées. Il n'est pas utile de les réimporter
"""

"""
Commencer par entrer les résultats de mesurage pour les mesurandes directes et les incertitudes types pour chaque source.
"""


"""
Créer les échantillons pour chaque source d'incertitude puis pour chaque mesurande directe.
"""
N = 100000


"""
Créer à partir des échantillons précédents, les échantillons simulés des mesurandes d, D puis f'.
Utiliser les instructions print des cellules précédentes pour afficher les résultats de mesurage
et incertitude-type associées à d, D et f'.

Appeler la distance focale f2 (et non f1) pour ne pas remplacer les échantillons de la méthodes de Descartes.
"""

"""
Représenter graphiquement l'histogramme des valeurs simulées.
"""


```

+++

### Compte-rendu des résultats.
Dans votre compte-rendu écrit, vous devez maintenant rendre compte des grandeurs de l'étude..

+++

### Exploitation des résultats avec Python

Utiliser la cellule ci-dessous pour calculer et afficher l'écart normalisé. Vous rendrez compte sur votre copie du résultat trouvé et commenterez la cohérence entre votre résultat d'expérience et le valeur constructeur.

```{code-cell} ipython3
:tags: [remove-output]
"""
On rappelle que les variables enregistrées à la cellule précédente sont encore en mémoire.
"""


```

## Combinaison des mesures (30mn)

+++

### Moyenne des mesures.
Utiliser la cellule de code ci-dessous pour calculer la moyenne des résultats de $f'$ obtenus par les deux méthodes. Pour cela, vous aller :
1. Faire N fois la moyenne des deux mesures pour les N échantillons simulés. Vous obtenez un vecteur de N simulations.
2. Obtenir ainsi le résultat de mesurage de $f'$ ainsi que son incertitude.

```{code-cell} ipython3
:tags: [remove-output]
"""
On rappelle que les variables enregistrées à la cellule précédente sont encore en mémoire.
"""


```

### Cohérence des mesures.
Réfléchir aux différentes cohérences entre valeur qu'on peut estimer (ici vous devez trouver au moins 3 écarts normalisés à calculer). Utiliser la cellule de code ci-dessous pour les calculer.

```{code-cell} ipython3
:tags: [remove-output]
"""
On rappelle que les variables enregistrées à la cellule précédente sont encore en mémoire.
"""


```

### Rendre compte et exploiter les résultats.
Rendre compte de la valeur moyenne de $f'$ ainsi que des deux résultats de mesurage obtenus par les méthode de Bessel et Descartes avec les incertitudes puis rendre compte des différents écarts normalisés. Exploiter ensuite ces mesures pour :
* tester la cohérence des méthodes entre elles
* tester la cohérence des méthodes et de la valeur finale avec la valeur constructeur
* comparer la précision des deux méthodes. A-t-on raison de faire une moyenne des résultats ?

## Conclusion
__Important__ : Les méthodes d'exploitation ont été très guidées pour ce premier TP. On remarquera ainsi qu'on a tester non seulement la compatibilité avec la valeur constructeur mais aussi la compatibilité des résultats des méthodes __entre elles__. On a aussi __comparer la précision__ des deux méthodes.

Ces exploitations ne sont pas les seules. On retiendra qu'il n'y a pas d'automatisme mais __qu'il est fondamental d'exploiter au maximum les résultats de mesures.__ Sans quoi votre travail n'aura servi à rien...

_Par la suite, les exploitations à réaliser ne seront pas forcément guidées comme pour ce TP._

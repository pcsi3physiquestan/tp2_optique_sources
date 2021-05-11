---
jupytext:
  encoding: '# -*- coding: utf-8 -*-'
  formats: ipynb,md:myst
  split_at_heading: true
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.1
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

Cette partie du TP constitue l'étude préliminaire qui doit être réalisée __avant le TP.__ Les questions posées doivent avoir une réponse écrite (vous pouvez tout à fait faire cette étude de manière manuscrite).

+++

# Etude préliminaire

+++

## Présentation rapide du matériel.

+++

### Présentation
Voici une liste non exhaustive du matériel que vous utiliserez en TP :
* __Banc d'optique et cavaliers__ : pour réaliser des montages en facilitant l'alignement des composants et pour réaliser des mesures de positions
* __Lentilles minces__
* __Miroir plan__
* __Lanterne et objet__ diaphragmant pour réaliser un objet lumineux
* __Viseur__ : Sert à mesurer la position d'objet ou la distance entre deux objets
* __Lunette afocale__ : Sert à étudier des objets à l'infini. On peut aussi s'en servir pour vérifier qu'un objet est bien à l'infini.
* __Collimateur__ : Sert à simuler un objet _étendu_ à l'infini.

Regarder la vidéo suivante pour obtenir quelques explications sur les premiers composants que vous allez utiliser (_Ne pas hésitez à mettre en pause la vidéo pour lire les explications_).

+++

```{code-cell} ipython3
---
tags: [remove-input]
---
from IPython.display import Video
Video("https://github.com/pcsi3physiquestan/tp2_optique/blob/main/notebook/videos/intru-divers.mp4?raw=true", width=640)
```

+++

### Analyse
Répondre (à l'écrit) aux questions suivantes:
1. Le cavalier palcé sur le banc optique permet de supporter une lentille, un objet, un écran... La mesure _directe_ par les graduations situées sur le banc optique donnent-elles une __position absolue__ de composant sur le banc optique ? ou un distance entre deux objets sur le banc optique ? Quelle conséquence cela aura sur l'estimation d'une incertitude d'une distance (par exemple une distance lentille-écran) ?
2. Pour déterminer rapidement le caractère convergent ou divergent d'une lentille, une méthode simple consiste à observer un objet lointain avec la lentille.
    1. Expliquer quel sens semi-quantitatif donner au terme __lointain__ pour une lentille de distance focale $f'$ ? Quelle approximation peut-on faire pour une étude théorique?
    2. Faire un schéma de tracé de rayon donnant l'image de l'objet lointain dans le cas d'une lentille convergente puis dans le cas d'une lentille divergente. Comment pourra-t-on faire la différence entre les deux?

+++

## Instruments d'optique

+++

### Présentation générale

On va maintenant présenter trois instruments particuliers : la lunette afocale, le collimateur et le viseur. Commencez par observer les trois vidéos de présentation du matériel ci-dessous (Exécutez la cellule). (_Pensez à mettre en pause la vidéo pour lire les explications._)

(etude_preliminaire:instru-lunette)=
```{code-cell} ipython3
---
tags: [remove-input]
---
Video("https://github.com/pcsi3physiquestan/tp2_optique/blob/main/notebook/videos/instru-lunette.mp4?raw=true", width=640)
```

(etude_preliminaire:instru-collimateur)=
```{code-cell} ipython3
---
tags: [remove-input]
---
Video("https://github.com/pcsi3physiquestan/tp2_optique/blob/main/notebook/videos/instru-collimateur.mp4?raw=true", width=640)
```

(etude_preliminaire:instru-viseur)=
```{code-cell} ipython3
---
tags: [remove-input]
---
Video("https://github.com/pcsi3physiquestan/tp2_optique/blob/main/notebook/videos/instru-viseur.mp4?raw=true", width=640)
```

### Exemple d'utilisation
Vous allez vous entrainer à utiliser ces instruments sur un cas simple : on veut déterminer la distance focale $f'$ d'une lentille grâce à un objet à l'infini. Répondez aux questions suivantes pour préparer le TP.

1. Si l'objet est à l'infini, où va se situer l'image par la lentille ? Comment peut-on alors mesurer simplement la distance focale ?
2. Parmi les trois instruments proposés, lequel (appelé instrument 1) permettra de simuler un objet à l'infini ? Lequel (appelé instrument 2) permettra de régler l'instrument 1 ?
3. Si l'on place un écran derrière la lentille pour y former l'image. Combien (et quelle ?) mesure(s) directe(s) doit-on faire pour obtenir la distance focale ? Préciser comment obtenir $f'$ de la (des) mesure(s) directe(s) réalisée(s).
4. On enlève l'écran. Bien regarder la vidéo du viseur. On doit réaliser deux visées pour pouvoir remonter à la distance focale $f'$. Que doit-on viser ? Que mesure-t-on lors de chaque visée ? Préciser comment on obtient $f'$ à partir des deux mesures réalisées grâce au viseur.
5. Si la lentille est divergente, peut-on encore utiliser un écran ? Peut-on encore utiliser un viseur ?
6. Reproduire l'énoncé du protocole suivant en remplaçant les trous par les termes adéquats. On observera la forme du protocole pour rédiger les suivants.
7. Dessiner un schéma de montage avec le protocole précédent. Vous devrez __toujours__ proposer un schéma du montage avec vos protocoles ensuite.
8. Réécrire le protocole et l'adapter à l'utilisation d'un viseur.

```{margin}
Ce protocole peut peut-être vous aider à répondre à certaines des questions précédentes si vous avez eu des difficultés.
```

#### Protocole à reproduire

__But__ : On désire mesure la distance focale d'une lentille.

__Principe__ : Si un objet à l'infini éclaire la lentille, son image va se situer ...... On peut donc estimer la distance focale de la lentille comme la distance ...............

__Mode opératoire__ (avec l'écran) :
1. On réalise le montage ci-dessous (vous devrez dessiner le schéma du montage).
2. Un .......... pour simuler un objet à l'infini. On place la lentille à étudier après le ............. (au plus près) puis un écran derrière la lentille.
3. On mesure sur le banc optique ................... (noté(e) $x_1$) et .................. (noté(e) $x_2$). La distance focale sera donc estimée comme $f' = x_1 - x_2$.

+++

## Focométrie

Le but du TP sera de mesurer de différentes manières la distance focale $f'$ d'une même lentille convergente. Dans un deuxième temps, on cherchera à estimer les incertitude sur ces mesures pour comparer leur efficacité entre elle et avec les données constructeur.

Vous allez dans cette étude préliminaire chercher à :
* comprendre les bases théoriques des différentes manipulations
* choisir quels instruments seront nécessaires pour la manipulation.
* mettre en place le protocole expérimental qu'il faudra réaliser.

+++

(etude_preliminaire:descartes)= 
### Utilisation des relations de Descartes.

On veut utiliser la relation de conjugaison de Descartes pour déterminer $f'$. On dispose d'un objet lumineux (à distance finie).

1. Rappeler la relation de conjugaison de Descartes des lentilles minces. En déduire que l'on peut obtenir une mesure de $f'$ en réalisant la mesure des distances $\overline{OA}$ et $\overline{OA'}$.
2. En pratique, on ne peut pas mesurer directement $\overline{OA}$ et $\overline{OA'}$. Si l'on utilise un écran pour former l'image, quels sont les mesurandes directs qui permettront de remonter aux distances $\overline{OA}$ et $\overline{OA'}$ ? Combien de mesurandes directes va-ton donc devoir mesurer ?
3. Si on enlève l'écran et qu'on utilise un viseur. Combien de visée devra-ton réaliser (et que vise-t-on pour chaque visée) ? Quel mesurande directe mesure-t-on à chaque fois. Expliquer comment remonter aux distances $\overline{OA}$ et $\overline{OA'}$.
4. Proposer un protocole utilisant la relation de conjugaison de Descartes et un écran permettant d'estimer la distance focale $f'$ d'une lentille convergente. Vous devrez bien présenter le __but__, le __principe__ puis le __mode opératoire__ en précisant quels sont les __mesurandes directes__ et comment on remonte à la grandeur voulue.
5. Proposer un protocole utilisant la relation de conjugaison de Descartes et un viseur permettant d'estimer la distance focale $f'$ d'une lentille convergente.
6. Si la lentille est divergente, peut-on encore utiliser l'un des protocoles précédents ? Si oui lequel ?

+++

(etude_preliminaire:bessel)= 
### Méthode de Bessel (ne faire que si vous avez bien compris la méthode précédente)

Le principe de la méthode de Bessel consiste à projeter l'image d'un objet à distance finie sur un écran à une distance $D$ de l'objet lumineux grâce à la lentille étudiée. Sous la condition de projection $D \geq 4f'$, on peut montrer qu'il existe deux positions $x_1$ et $x_2$ de la lentille qui permettent la projection et que l'on a une relation entre $d = x_2 - x_1 > 0$ et $D$ :

$$
1 - {\left ( \frac{d}{D}\right)}^2 = 4 \frac{f'}{D}
$$

__Cette relation a été démontrée en exercice lors de l'étude de la projection. Il est vivement conseillé de s'entraîner à la démontrer mais ce n'est pas l'objet du TP.__

1. Expliquer comment mesurer $D$. On précisera combien de mesurandes directs il faut mesurer et comment on remonte à $D$.
2. Expliquer comment mesurer $d$. On précisera combien de mesurandes directs il faut mesurer et comment on remonte à $d$.
3. Exprimer $f'$ en fonction de $d$ et $D$.
4. Rédiger proprement le protocole de la manipulation. Vous devrez bien présenter le __but__, le __principe__ puis le __mode opératoire__ en précisant quels sont les __mesurandes directes__ et comment on remonte à la grandeur voulue.
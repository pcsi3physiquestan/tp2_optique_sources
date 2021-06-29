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

On va commencer par réaliser les expériences sans se soucier des incertitudes de mesure pour apprendre à utiliser le matériel d'optique. Le compte-rendu est un compte-rendu écrit qui fera suite à l'étude préliminéaire précédente.

+++

# (TP) Présentation rapide du matériel

```{margin}
Cette partie fait suite à l'étude préliminaire du même nom.
```

+++

## Détermination rapide du type de lentille (20mn)
On se propose d'utiliser deux méthodes pour déterminer le type de lentille :
* sa forme
* l'observation d'un objet lointain.

Prenez deux lentilles de distance focale connues, l'une convergente et l'autre divergente.

+++

### Forme de la lentille
1. Observer la forme des deux lentilles et commenter la concavité des deux faces. Expliquer comment faire la différence entre une lentille convergente et une lentille divergente.

```{margin}
Cette méthode n'est pas toujours satisfaisante car la détermination des concavités des faces n'est pas toujours évident.
```

+++

### Observation d'un objet lointain.

2. Observer un objet lointain. Grâce à l'étude préliminaire, vérifier que vous pouvez distinguer une lentille convergente d'une lentille divergente. Expliquer clairement la méthode.
    1. _Question supplémentaire_ : Pourquoi faut-il tendre le bras quand on observe à travers une lentille convergente ?
3. Prendre une lentille de distance focale inconnue et déterminer son type. Rendre compte de votre étude.

+++

## Instruments d'optique (40mn)

```{margin}
Cette partie fait suite à l'étude préliminaire du même nom.
```

Pour cette partie et pour les suivantes, vous prendrez toujours __la même lentille convergente__ de manière à pouvoir comparer les méthodes et leur précision par la suite.

+++

### Exemple d'utilisation.

Rappel : On veut déterminer la distance focale d'une lentille convergente en utilisant un objet à l'infini qu'on va simuler.

+++

#### Utilisation d'un écran

Les vidéo des réglages sont disponibles [ici](etude_preliminaire:instru-lunette)

1. Régler l'instrument 2 choisi dans l'étude préliminaire.
2. Utiliser l'instrument 2 pour régler l'instrument 1 (_utiliser une lentille de distance focale +50mm et l'objet de précision pour construire l'instrument 1_).
3. Réaliser le reste du montage en utilisant le schéma de montage que vous avez proposé.
4. Mesurer les deux grandeurs $x_1$ et $x_2$ choisie dans votre protocole et en déduire $f'$. _Si aucun calcul d'incertitude n'est demandé, commencer à observer les éléments qui causent une variabilité de la mesure._

+++

#### Utilisation d'un viseur.
```{margin}
Cette fois, certaines réponses quant au protocole sont données, servez-vous en pour vérifier votre protocole.
```

1. __Pensez à enlever l'écran.__
2. Viser la lentille (un des bords) avec le viseur et mesurer la première grandeur notée $x_{v1}$
3. Reculer le viseur pour viser l'image avec le viseur et mesurer la deuxième grandeur notée $x_{v2}$. _Si aucun calcul d'incertitude n'est demandé, commencer à observer les éléments qui causent une variabilité de la mesure._
4. En déduire $f'$.

+++

#### Comparaison qualitative.
Sans entrer dans le détail des estimations, commenter les éléments qui occasionnent une incertitude sur les mesures de $x_1$ et $x_2$ puis de $x_{v1}$ et $x_{v2}$. D'après vous, quelles mesures seront les moins incertaines ?

+++

### Conclusion
Vous avez ainsi appris à utiliser les trois instruments principaux : lunette, collimateur et viseur.

```{important}
On retiendra :
* La méthode d'utilisation du viseur pour mesurer une distance entre deux objets grâce à deux mesures de position __du cavalier du viseur.__
* Les intérêts du viseur dans les mesures de distance.
* La méthode de réglage d'une lunette et son utilisation pour régler un collimateur.
```

+++

# (TP) Focométrie : Etude semi-quantitative

## Utilisation des relations de Descartes (1h)

Vous allez réaliser le protocole que vous avez mis en place dans [l'étude préliminaire](etude_preliminaire:descartes).

1. Réaliser le protocole et rendre compte des résultats de mesurage (sans leur incertitude) pour chaque mesurande directe.
2. Déduire les distances algébriques $\overline{OA}$ et $\overline{OA'}$ puis la distance $f'$. Rendre compte du résultat obtenu. Commenter

```{margin}
L'exploitation des résultats restera ici succinte puisqu'on n'a pas estimé les incertitudes.
```

## Utilisation des relations de Bessel (1h)

Vous allez réaliser le protocole que vous avez mis en place dans [l'étude préliminaire](etude_preliminaire:bessel).

1. Réaliser le protocole et rendre compte des résultats de mesurage (sans leur incertitude) pour chaque mesurande directe.
2. Déduire les distances $d$ et $D$ puis la distance $f'$. Rendre compte du résultat obtenu. Commenter

```{margin}
L'exploitation des résultats restera ici succinte puisqu'on n'a pas estimé les incertitudes.
```
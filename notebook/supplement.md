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

Attention, cette partie n'est à réaliser __QUE si vous avez bien compris les parties précédentes.__ Comptez au moins 1 heure pour réaliser les mesures de chaque partie. L'exploitation peut être réalisée chez vous ensuite.

# Détermination d'une distance focale pour une lentille divergente.

Prenez une lentille divergente de focale relativement grande. Vous devez proposer une adaptation des protocoles précédents pour mesurer la distance focale de la lentille :
* en utilisant un objet à l'infini (simulé)
* en utilisant un objet à distance finie et les lois de Descartes

A vous de voir si le protocole peut être utilisé directement ou s'il nécessite des adaptations, si certaines précautions supplémentaires sont nécessaires. Une cellule de code est disponible ci-dessous pour réaliser vos traitements pour les incertitudes (le document est téléchargeables comme précédemment).

```{code-cell} ipython3
"""
Cellule de code pour le traitement des données relatives à l'étude d'une lentille divergente.
"""


```

# Utilisation d'une régression linéaire
Reprendre la même lentille convergente que pour l'étude initiale. On veut réaliser non plus une mesure de $d$ en fixant $D$ avec la méthode de Bessel mais plusieurs (on fera cinq mesures pour 5 valeurs différentes de $D$). L'idée est retrouver la distance focale $f'$ comme la pente d'un ajustement affine reliant deux grandeurs $x(d, D)$ et $y(d, D)$. Proposer puis réaliser un protocole permettant d'obtenir $f'$ de cette manière.

La cellule de code ci-dessous vous permettra de réaliser la régression linéaire. N'hésitez pas à utiliser ce qui a été vu dans le premier TP pour réaliser la régression linéaire sous Python et obtenir l'incertitude sur $f'$.

```{code-cell} ipython3
"""
Cellule de code pour le traitement des données relatives à l'étude d'une lentille convergente par la méthode de Bessel.
"""


```
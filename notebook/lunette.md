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

Cette partie du TP est complètement indépendante des précédentes. Vous allez apprendre à manipuler les notions en rapport avec les objets à l'infini. Cette partie est peu guidée. C'est à vous de :
* proposer un protocole répondant aux problématiques posées.
* réaliser ce protocole et réaliser les bilans d'incertitude nécessaires.
* exploiter les mesures que vous aurez obtenus pour répondre aux problématiques posées.

Ce notebook est téléchargeable en versino `.ipynb` grâce au bouton ![Bouton téléchargerment](./images/bouton_tl.png). _On rappelle qu'il faut choisir le format `.ipynb` et le placer dans un répertoire adapté pour l'ouvrir avec Jupyer Notebook_).

+++

# Etude d'une lunette astronomique. (1h)

Une lunette de Galilée est une lunette astronomique, c’est-à-dire destinée à viser des objets à l’infini, dont le dispositif oculaire est un système divergent. Nous allons chercher à construire une lunette de Galilée destinée à être utilisé par un oeil emmétrope dans les meilleurs conditions. Dans son modèle le plus simple, une lunette de Galilée est constituée :
* d’un objectif réalisé par une lentille convergente
* d’un oculaire réalisé par une lentille divergente

+++

## Cahier des charges de la lunette
* La lunette de Galilée construire devra satisfaire la description précédente.
* De plus, une lunette sert à grossir les objets observés pour mieux en visualiser les détails. Si les grossissements des lunettes du commerce peuvent atteindre $\times 10$ à $\times 400$, nous nous contenterons ici d’un faible grossissement (à cause des faibles diamètres de la lentille). On impose donc que le grossissement soit compris entre 1,4 et 2.
* La lunette devra être utilisée par l’oeil humain emmétrope ou avec ses défauts. On la testera avec un oeil au repos modélisé par __un système lentille + écran avec une lentille +200mm__.
* Pour régler la lunette, on fait "comme s'il s'agissait d'une vraie lunette" : on ne peut pas la démonter pour mesurer les distances focales des lentilles (qui ne sont connues qu'à 10%). __On devra donc proposer un protocole de réglage de la lunette par l'utilisateur (l'oeil emmétrope) sans connaître les distances focales.__

+++

## Matériel à disposition
* 1 Banc optique
* 6 Cavaliers (différents régagles sont possibles sur les cavaliers)
* 4 Porte-objet/lentilles
* 1 Objet lumineux LED
* 1 Objet de précision
* 1 Lunette afocale
* 1 Ecran
* 3 Lentilles sur pieds (Valeurs indicatives, __elles peuvent changer le jour du TP__ : +100mm ; +200mm, -100mm)
* 4 Lentilles sans pieds (Valeurs indicatives, __elles peuvent changer le jour du TP__ : +50mm +150mm ; +300m ; -300mm)
* 1 Miroir Plan

## Oeil emmétrope au repos
Proposer un protocole permettant de simuler l'oeil emmétrope au repos constitué de la lentille de focale +200mm et d'un écran. Procéder ensuite à la réalisation de cet oeil emmétrope.

## Lunette de Galilée
Vous devez maintenant :
1. Choisir des distances focales adaptées pour construire une lunette de Galilée répondant au cahier des charges.
2. Proposer puis réaliser un protocole pour régler la lunette et la rendre utilisable par l'oeil emmétrope au repos construit précédemment. __On rappelle que vous devez partir du principe que vous ne connaissez pas les distances focales des lentilles pour ce réglage.__
3. Proposer puis réaliser un protocole permettant de mesurer le grossissement de la lunette ainsi construite. On devra vérifier l'adéquation entre la valeur mesurée et le cahier des charges.

```{code-cell} ipython3
"""
Utilisez cette cellule pour réaliser les simulations de Monte-Carlo adéquates et obtenir les incertitude de mesure que vous devez calculer.

Attention, les bibliothèques scientifiques n'ont pas été chargées. Vous êtes complètement libre dans votre traitement.
"""


```

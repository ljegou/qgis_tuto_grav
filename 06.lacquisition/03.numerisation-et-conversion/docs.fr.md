---
title: 'Conversion et numérisation'
taxonomy:
    category:
        - docs
---

De nos jours, de nombreuses données spatiales d'archive ont déjà été numérisées. Cependant, il reste certains documents qui ne sont disponibles qu'en version analogique ou, plus souvent, simplement scannées et non référencées.

Un des enjeux importants demeure la reconnaissance des informations spatiales dans des contenus textuels, par exemple le repérage et le géocodage des adresses dans des informations alphanumériques, produites par des systèmes qui ne tiennent pas compte de la géographie (saisie par les utilisateurs, numérisation simple).

Enfin, il existe aussi le cas où l'on crée de l'information à partir de l'observation de terrain ou en se basant sur des fonds de cartes dépassés, nous verrons donc comment saisir directement de nouvelles données spatiales vectorielles dans QGIS.

Dans cette partie, nous verrons donc rapidement, avec QGIS, comment :
* **Reconnaître** des références spatiales textuelles (colonnes de coordonnées)
* **Géocoder** des adresses
* **Géoréférencer**, caler des photographies numérisées
* **Saisir** des données spatiales directement, à partir d'un fond de référence.
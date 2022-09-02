---
title: 'Description des fonctions'
taxonomy:
    category:
        - docs
---

##Acquisition

L'**acquisition** regroupe les opérations qui permettent de créer ou de convertir de l'information numérique spatiale en vue de son intégration dans un SIG.

On y décrira les points suivants :
* **GPS** et outils de positionnement sur le terrain
* **Numérisation** de données analogiques, saisie directe et calage d'images
* **Géocodage** automatique d'adresses

## Intégration et structuration

Ces deux opérations concernent la prise en compte de données dans les SIG, par conversion, transformation, adaptation ou traduction. Pour les cas courants de données, elles sont automatisées grâce à l'utilisation de briques logicielles centrales dans les SIG qui effectuent les conversions et reprojections de données, essentiellement [GDAL/OGR](https://gdal.org/) et [PROJ](https://proj.org/).

QGIS s'en chargera donc directement, pour l'enssentiel (outre la connexion à des bases existantes). On fera donc quelques recommendations de formatage et de maintenance des projets avec QGIS.

## Traitement de données et interprétation

Il s'agit là, logiquement, du cœur des fonctionnalités d'un SIG, la partie où le système va pouvoir répondre à des questions, créer de nouvelles données par croisement et enrichissement. Nous examinerons des exemples et réaliserons quelques opérations de croisement d'information, requêtage et enrichissement.

## Mise en forme de résultats et communication

Ces deux fonctions seront logiquement regroupées, car elles correspondent à la réalisation de documents de présentation de résultats, de planche cartographiques, et à leur diffusion, sous la forme d'images ou de cartes interactives sur le web.

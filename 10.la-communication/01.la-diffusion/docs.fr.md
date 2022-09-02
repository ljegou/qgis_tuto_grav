---
title: 'La diffusion : principes'
taxonomy:
    category:
        - docs
---

La diffusion est un domaine qui reprend de l’importance de nos jours, grâce aux supports numériques (dont mobiles) et aux services web de mise à disposition de données et de cartes.

Par exemple : QGIS Cloud [https://qgiscloud.com/](https://qgiscloud.com/)

Un SIG moderne possède des capacités de diffusion web, ou est compatible avec des outils complémentaires de diffusion grâce à **un système de webservices normalisés**, selon des standards définis par l’[Open Geospatial Consortium (cf. la documentation de GéoBretagne)](https://cms.geobretagne.fr/content/quest-ce-quun-service-web-ou-flux-ogc).

Pour ce faire, QGIS possède une **version serveur**, que l'on peut donc installer sur un serveur web et qui va utiliser des fichiers projets pour configurer des webservices selon les normes OGC : [cf. la documentation officielle](https://docs.qgis.org/3.10/fr/docs/training_manual/qgis_server/index.html).

Des extensions existent pour générer directement des projets web depuis QGIS, comme « [QGIS2Web](https://github.com/tomchadwin/qgis2web) ».

De mnière plus complète, le projet open-source [LizMap](https://www.3liz.com/lizmap.html) propose un plugin QGIS qui permet de configurer une partie serveur qui va piloter et encapsuler QGIS serveur pour proposer **une véritable application SIG interactive** cliente, très complète (avec légende, moteur de recherches, fonds au choix...).

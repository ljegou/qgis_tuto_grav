---
title: 'En conclusion'
taxonomy:
    category:
        - docs
---

Cette introduction aux systèmes d'information géographique avec QGIS avait pour but de présenter les données spatiales, leur traitement et leur représentation, de manière simple, à destination des débutant.e.s.

Le domaine des SIG et le logiciel QGIS sont bien plus larges et proposent des fonctionnalités avancées, utilisées dans des cadres professionnels.

### Domaines qui n'ont pas été couverts par la formation

De nombreux domaines, trop complexes pour convenir à une introduction, n'ont pas été présentés ici.

Les plus importants sont :
* La connexion à des serveurs de bases de données ou de webservices.
* Les traitements avancés, comme les opérations vectorielles complexes (calculs d'itinéraires, génération d'entités...), les analyses d'images... 
* Les traitements et la représentation en 3D (covisibilité, vues en perspective)
* Les requêtes complexes en SQL
* L'automatisation des procédures avec le modeleur graphique
* La programmation pour automatiser des traitements ou développer des extensions en langage Python

### Des pistes pour aller plus loin

La [documentation officielle de QGIS](https://docs.qgis.org/3.10/fr/docs/user_manual/index.html) couvre une grande partie de ces domaines, c'est la première référence à consulter.

Les greffons ou extensions (*plug-ins*) sont très nombreux et permettent d'étendre les fonctionnalités du logiciel dans de nombreux domaines.

On peut les installer facilement en utilisant le menu "Extensions", qui se connecte aux dépôts officiels en ligne. Ces dépôts sont vérifiés et validés par la communauté. Vous pourrez trouver la liste des extensions et leur description [sur le site de QGIS](https://plugins.qgis.org/). 

D'autres sources d'extensions existent, directement sur le site de leurs auteurs, par exemple ceux d'[Alex Bruy](https://plugins.bruy.me/plugins/plugins.xml) (dont les Whitebox Tools, pour traiter les données Lidar et réaliser des analyses géostatistiques). Actuellement, ces plugins ne sont plus disponibles, l'auteur refusant qu'ils puissent être employés pour des activités militaires (03/2022).

Ensuite, vous pourrez trouver certains tutoriels complémentaires sur des sites spécialisés, par exemple :
* [NaturaGIS](https://naturagis.fr/tutoriels-sig/qgis/)
* [Sigea](https://sigea.educagri.fr/tutos-sig/tutos-qgis)
* [ENSG](http://cours-fad-public.ensg.eu/course/view.php?id=37)
* [SigTerritoires](https://www.sigterritoires.fr/index.php/tutoriels-2/tutoriels-qgis/)
* [UMR Passages (J. Pierson)](https://ouvrir.passages.cnrs.fr/tutoqgis/)
* [Guide d'utilisation QGIS 3.4 du CEN-Normandie](https://si.cenlr.org/sites/si.cenlr.org/files/Guide_QGIS_3.4.pdf)

Quelques idées pour découvrir un peu plus complètement QGIS :
* Explorer la fenêtre de la *boîte à outils des traitements*.
* Découvrir plus complètement les *menus* du logiciel, notamment "Vecteur" et "Raster", avec des couches de données d'exemple ouvertes.
* Détailler les fonctions disponibles dans le *calculateur de champs* et l'*outil de sélection d'entités selon une expression*.
* Passer en revue les différentes *extensions*, officielles et complémentaires.
---
title: 'Composer une mise en page'
media_order: 'nvelle_mep.jpg,mep_vide.jpg,mepc.m4v,mep_export_formats.jpg'
taxonomy:
    category:
        - docs
---

Les représentations cartographiques étant paramétrées par les propriétés des couches, il faut donc utiliser un outil spécifique pour **mettre en page une véritable planche cartographique**, c'est le rôle de la fonction de mise en page (anciennement connue sous le nom de *composeur d'impression*) de QGIS.

## Préparer une planche cartographique

On accède à cette fonctionnalité via le menu "Projet", puis "Nouvelle mise en page".

![Nouvelle mise en page](nvelle_mep.jpg?lightbox=1024&cropResize=400)

Comme QGIS est capable de gérer plusieurs mises en pages (et de les sauvegarder pour leur réutilisation), il nous demande de lui donner un nom.

La fenêtre de mise en page possède ses propres menus et barres d'icônes, assez fournis. À droite se trouvent des onglets permettant de paramétrer la mise en page dans son ensemble (grilles, export), d'afficher les propriétés de l'objet actuellement sélectionné et de régler les lignes-guides (repères).

Le format matériel de la page se règle par le menu "Mise en page", "Format de la page". Pour notre exemple, choisissons un format A4 à l'horizontale (paysage ou à l'italienne).

![Écra&n de MEP vide](mep_vide.jpg?lightbox=1024&cropResize=600)

La colonne d'icônes de gauche présente les outils pour ajouter (petit "plus") et manipuler (flèches) les items d'une mise en page comme :

Des **élements indispensables** :
	* Une carte (qui sera une copie de l'écran carte de QGIS)
	* Une légende
	* Une échelle
	* Une flèche de Nord (ou orientation)
	* Des sources (données statistiques et spatiales, comme le fond de carte utilisé)
<br><br>

Des **éléments d'habillage**, optionnels, comme :
	* Une image (photo, logo...)
	* Des formes (rectangle, ellipse, cadre)
	* Des symboles
	* Des flèches
	* Des libellés ou petits paragraphes de texte
	* Une table d'attributs (mais souvent la place manque)
	* Une zone de texte au format HTML

Pour préparer notre planche cartographique, à partir de notre dernière carte en plage de couleurs réalisée dans QGIS, on va donc devoir suivre les étapes suivantes (décrites dans la vidéo ci-après) :
* Ajouter et dimensionner la **carte**
* Ajouter la **légende**
* Ajouter une **échelle** graphique
* Ajouter un **titre** et des **sources**

![mepc.m4v](mepc.m4v)

Pour améliorer cette mise en page, il est possible de modifiser certaines apparences :
* Choisir une *échelle graphique* plus fine (barre avec barbules plus simples)
* Utiliser des *enrichissements stylistiques* pour le titre (taille de police, gras et italiques)
* Ajouter des éléments de *repérage géographique* comme des points et libellés pour les grandes villes ou les EPCI présentant des valeurs intéressantes (positives ou négatives), dans le but d'aider à l'interprétation de la carte.
* Ajouter un *nom d'auteur et une date de réalisation*, sous les sources.

## Exporter une planche

Pour sortir cette mise en page de QGIS et produire un document numérique indépendant, il faut utiliser les fonctionnalités d'export. Deux formats vectoriels sont à notre disposition : le SVG, libre et compatible avec les navigateurs web et les logiciels de dessin vectoriel (comme [InkScape](https://www.inkscape.org)), ou le PDF, compatible avec les lecteurs de documents.

![Formats d'export de la mise en page](mep_export_formats.jpg?lightbox=1024&cropResize=300)

Ces deux formats sont accessibles via le menu "Mise en page" ou les icones, ainsi qu'un format image raster (pixels).
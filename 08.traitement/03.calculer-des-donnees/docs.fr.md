---
title: 'Calculer des données'
media_order: 'icone_calc.jpg,trat_calc2.jpg,trat_calc1.jpg'
taxonomy:
    category:
        - docs
---

Un autre outil de traitement de l'information des SIG concerne le calcul de nouveaux champs à partir de ceux existants. QGIS propose, pour ce faire, une calculatrice avancée qui va faciliter la réalisation de calculs, mais il est aussi possible d'utiliser des requêtes directement en langage SQL ou python. Notez que QGIS permet aussi le calcul de champs temporaires dans certaines opérations, notamment de traitement et de représentation cartographique.

## Calcul de nouveaux indicateurs numériques

Les données statistiques que nous avons jointes à la couche des EPCI lors de l'étape précédente contiennent le nombre d'emplois au lieu de travail dans ces regroupements de commune, en 2013 et en 2018. À partir de ces deux années, on peut calculer une évolution brute et un taux d'évolution relative, on peut très bien réaliser ce calcul directement dans QGIS.

Pour ce faire, nous allons utiliser l'outil de "calculateur de champs" du logiciel, en prenant soin d'avoir sélectionné la couche des EPCI au préalable :
![Icone calculateur de champs](icone_calc.jpg)

### Calcul de l'évolution brute du nombre d'emplois entre 2013 et 2018

Le calculateur de champs nous demande d'abord si nous voulons créer un nouveau champ ou en modifier un existant, puis comme nous voulons créer un nouvel attribut, il nous en demande le nom et le type.

Comme l'évolution brute est la simple différence entre les valeurs des deux années, et que ces dernières contiennent des valeurs entières (ce ne sont pas des estimations), on peut choisir le type des entiers.

Ensuite, il faut entrer la formule dans la partie gauche de l'éditeur d'expressions, ce qui est facilité par les colonnes de la partie droite qui proposent les listes des champs et fonctions utilisables, ainsi que la description des opérations, un apreçu des valeurs des champs utilisés et du résultat de l'expression (avec notamment un message d'erreur si celle-ci est incorrecte).

Enfin, tout en bas de la fenêtre, QGIS nous prévient que la couche n'est actuellement pas en mode édition (autorisation des modifications), donc que l'exécution de ce calcul de nouvau champ va ouvrir ce mode édition pour cette couche. Ainsi, en cas d'erreur de calcul, il suffira d'annuler les modifications pour retrouver la couche des EPCI dans son état d'origine.

![Calculateur d'expression pour évolution brute 2013-2018](trat_calc1.jpg?lightbox=1024&cropResize=800,600)

### Calcul de l'évolution relative, le taux en % entre 2013 et 2018

Le calcul du taux se réalise de manière semblable, en prenant soin de :
* Donner un nom explicite au  nouveau champ
* Choisir le type "nombre décimal ('réel')" avec quelques décimales de précision
* Utiliser la formule qui produit un pourcentage d'évolution

![Calculateur d'expression pour évolution relative 2013-2018](trat_calc2.jpg?lightbox=1024&cropResize=800,600)
---
title: 'Joindre des données'
media_order: 'joint_csv.jpg,joint_epci_emplois_table.jpg,joint_epci_emplois.jpg'
taxonomy:
    category:
        - docs
---

La réalisation de traitements géomatiques sur des couches différentes, dont l'une d'elle n'est pas géoréférencée, implique de pouvoir indiquer au système comment les couches peuvent être *reliées* entre elles, l'information qu'elles partagent.

Par exemple, on peut chercher à joindre des données statistiques à une couche de zonage administratif (IRIS, quartiers, communes, dépatements...) ou rechercher les éléments communs à deux couches spatiales (les communes à la fois en zone de risque d'inondation et de risque industriel). Dans le jargon des bases de données, on appelle ces relations des ***jointures***.

Dans les SIG, on peut donc réaliser deux types de jointures :
* les *jointures attributaires*, un attribut est commun entre les couches à relier (généralement des identifiants comme les géocodes)
* les *jointures spatiales*, où une caractéristique géographique (de position/extension) va servir de relation : inclusion, croisement, contiguité, superposition, proximité ou distance...

## Jointure attributaire : ajouter des attributs à une couche spatiale

Très souvent, les couches de données spatiales ne sont fournies qu'avec des attributs simples, des identifiants. Pour effectuer des traitements, par exemple avec des données statistiques, puis représenter le résultat sous forme de carte, il faut donc *relier* ces données géographiques avec des données statistiques, qui sont, quant à elles, généralement fournies sous la forme de tableaux alphanumériques simples (XLS, CSV...).

La *jointure attributaire* va permettre de demander à QGIS de recopier les données d'une table alphanumérique dans la table attributaire d'une couche spatiale, en utilisant une colonne d'identifiants commune aux deux couches de données. On utilise pour cela des codes d'identification uniques (comme les codes INSEE pour les communes) pour éviter les problèmes de noms en double (par exemple, il existe 2 communes nommées "Aucamville", dans la Haute-Garonne et le Tarn-et-Garonne, distantes de seulment 20 kms).

**Attention** : Cette opération ne peut donner de bons résultats que si les conditions suivantes sont réunies :
* Les champs contenant les identifiants sont **de même type** dans les deux sources de données (numérique / texte notamment).
* Les données tabulaires correspondent à tout ou partie des entités de la couche géographique (il peut y avoir des manques ou des surplus, d'un côté ou de l'autre, mais pas de doublons).

### Pratique avec QGIS : ajout d'informations sur les emplois à la couche des EPCI

* Charger la couche (si elle ne l'était pas déjà) vectorielle des EPCI de Midi-Pyrénées : *epci_mp21.shp*  
	* Menu Couche / Ajouter une couche / Vectorielle  


* Ouvrir le fichier CSV (texte délimité, comme précédemment dans le chapitre sur l'acquisition, mais sans colonnes de coordonnées lat/long, cette fois) : *EPCI_nb_emplois_evo_2013-2018.csv* (Notez la page de code du fichier source : *UTF-8* et la présence d'un fichier .CSVT qui définit les types des champs de ce fichier CSV).
	* Menu Couche / Ajouter une couche / Texte délimité
![Ouvrir texte délimité simple](joint_csv.jpg?lightbox=1024&cropResize=800,600)


* Dans les propriétés de la couche EPCI_mp21 (double-clic ou clic droit sur la couche en légende), réaliser la jointure avec ce fichier, en utilisant les géocodes : CODE_EPCI = CODE_EPCI, comme sur l'image ci-dessous. Notez le paramètre qui permet de définir le préfixe ajouté aux nouveaux champs (ici, *aucun*, les noms des champs de la source tabulaire sont assez explicites sans préfixe).

![Propriétés table EPCI, jointure emplois CSV](joint_epci_emplois.jpg?lightbox=1024&cropResize=800,600)

On peut vérifier la présence des nouvelles données attributaires en affichant la table :

![Table attributs des EPCI après la jointure des emplois](joint_epci_emplois_table.jpg?lightbox=1024&cropResize=800,600)

**Attention** : ces nouvelles données attributaires, ajoutées à la table des EPCI, ne le sont qu'en mémoire dans le projet QGIS en cours. Si vous voulez retrouver ces données sans avoir à réétablir la jointure, il faut enregistrer le projet ou, plus définitivement, enregistrer la couche EPCI sous un autre nom pour écrire les données sous la forme de fichiers.

Nous verrons les jointures spatiales dans le cadre des requêtes, un peu plus loin dans la formation.


---
title: 'Introduction et exemples'
media_order: 'trat_ex1.jpg,trat_ex2.jpg,trat_ex2_ContraintesTechniquesUrbaines_17_StJeanDeLiversay.jpg,trat_ex2_nordex.jpg,trat_ex2_photovoltaique.jpg,trat_ex2_photovolt1.jpg,trat_ex2_photovolt2.jpg,trat_ex2_commerce_metz.jpg,trat_ex2_risques.jpg'
taxonomy:
    category:
        - docs
---

Le cœur du travail en géomatique, la partie la plus directement "productive" des SIG, concerne les traitements de données. Une fois celles-ci acquises, organisées et structurées, on peut les utiliser pour étudier une question, observer un territoire, illustrer un exposé...

Voici quelques exemples qui balayent les fonctionnalités courantes des SIG.

## Création d'indicateur spatialisé : les isochrones

Les isochrones sont des lignes d'égale durée de parcours à partir d'une entité spatiale (point, ligne ou polygone), on les utilise pour observer la couverture d'une région par les moyens de transport, par exemple.

![Exemple de traitement, isochrones OIN Orly-Rungis](trat_ex1.jpg?lightbox=1024&cropResize=400,400)
Voici l'exemple des isochrones de déplacement à pied à partir des arrêts du Tram-Train et du RER, dans la zone de l'[Opération d'Intérêt National Orly-Rungis](https://www.epa-orsa.fr/), au sud de Paris. À partir de la couche des voies de ces deux réseaux de transport en commun, ainsi que de la couche du réseau des rues, le SIG a calculé de nouvelles données spatiales : les surfaces accessibles à pied en 5 et 15 minutes (en posant une hypothèse moyenne de vitesse de ce déplacement).
Comme le SIG gère la spatialité des données, il est capable de localiser des gares et des axes de transport et d'établir à partir de ces entités de nouveaux polygones en réalisant une conversion temps de parcours / distance dans l'espace en suivant un réseau de lignes (les rues).

## Création de zones, croisement d'information : une analyse pour la localisation d'éoliennes

Le développement de l'énergie verte, notamment éolienne, est fortement demandeur de compétences en géomatique, car la recherche d'opportunités naturelles et le contexte règlementaire rendent l'utilisation et le croisement de données spatiales très importants. On retrouve ces analyses dans les études d'impact des projets éoliens.

Le croisement des données permet de rechercher des zones propices du point de vue de la ressource (vents, orientation, proximité des lignes élctriques et des centres de distribution) et des contraintes humaines et règlementaires (habitations, voirie, zones de protection du patrimoine, espaces naturels).

Voici deux exemples illustrés.
![Enjeux projet éolien Lavausseau](trat_ex2.jpg?lightbox=1024&cropResize=400,400)  
Source : Société Valorem

Dans cet exemple, sont surtout prises en compte les habitations, la loi imposant une distance d'au moins 500m entre une éolienne et une construction d'habitation. Le SIG a permis de définir la zone interdite, en jaune, et la zone possible, en bleu. Ces cercles de 500m de rayon  autour des habitations sont appellés, dans le jargon des SIG, des "zones tampon" ou *buffers*, en anglais, on verra dans la prochaine partie comment en produire avec QGIS.

![Enjeux techniques projet éolien de Liversay](trat_ex2_ContraintesTechniquesUrbaines_17_StJeanDeLiversay.jpg?lightbox=1024&cropResize=400,400)  
Source : [site du projet par Volkswind](https://parc-eolien-st-jean-de-liversay.fr/)

Ici, plusieurs contraintes sont prises en compte, les habitations (en rouge), comme précédemment, mais aussi les voies de communication (qui produisent des zones tampon allongées, tubulaires, le long des routes), la proximité d'une ligne à haute tension (en mauve, positive, intéressante pour réduire les distances de connexion des éoliennes), la présence d'un faisceau de micro-ondes ANFR (en rose foncé) et la proximité d'une piste de décollage de petits avions (ULM, en rose à l'est de la carte).


![Enjeux techniques Nordex Coatjégu](trat_ex2_nordex.jpg?lightbox=1024&cropResize=400,400)
Source : Société Nordex

Enfin, dernier exemple de projet éolien, avec cette fois la présence d'une forêt (oiseaux à protéger).

## Création de zones, croisement avec des données de boisement et de relief : les projets photovoltaïques

Toujours dans le cadre des projets d'énergies vertes, le cas des parcs de capteurs photovoltaïques est intéressant car la ressource en ensoleillement présente de nouvelles contraintes : l'ombre et l'orientation. La contrainte visuelle (ne pas gâcher le paysage) est aussi assez forte et nécessite de prendre en compte le relief et les écrans visuels (comme les bois et les haies).

![Enjeux paysagers projet photovoltaique relief](trat_ex2_photovolt2.jpg?lightbox=1024&cropResize=400,400)
Source : Société Sun'R

![Enjeux paysagers projet photovoltaique bois](trat_ex2_photovoltaique.jpg?lightbox=1024&cropResize=400,400)
Source : Société Luxel

## Géomarketing : Croisement de l'accessibilité et de l'offre

L'utilisation des données spatiales est importante dans le domaine de la planification et de l'optimisation commerciale, que l'on appelle aussi le *géomarketing*. On peut, par exemple, rechercher les meilleures localisations pour de nouveaux magasins en croisant plusieurs critères, comme l'accessibilité routière par les clients et la présence de concurrents.

Dans la carte de Metz ci-dessous, réalisée par la [société Articque](https://www.articque.com/creer-une-zone-de-chalandise/), on trouve un exemple de ce type d'analyse, qui met en évidence une zone accessible et potentiellement non équipée au nord de l'agglomération messine.

![Géomarketing d'implantation à Metz](trat_ex2_commerce_metz.jpg?lightbox=1024&cropResize=400,400)
Source : Artique

## La gestion des risques : croiser aléas et enjeux

La prévention et la gestion des risques est un autre domaine dans lesquels les SIG sont très utilisés. Au cœur des réflexions se trouve le croisement entre des aléas (des évènements dangereux imprévisibles, d'origine naturelle ou industrielle) et des enjeux (les éléments qui sont sensibles au risque : les populations, les activités, le patromoine...).

![Synthèse des risques d'inondation IAU expé. nord 92](trat_ex2_risques.jpg?lightbox=1024&cropResize=400,400)
Source : [IAU, expérimentation de la boucle du nord des Hauts-de-Seine](https://www.institutparisregion.fr/fileadmin/NewEtudes/Etude_1391/Rapport_Gennevillier_VF2_Juillet2017_b.pdf)



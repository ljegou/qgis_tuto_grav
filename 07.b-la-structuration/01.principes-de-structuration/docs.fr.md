---
title: 'Principes de structuration'
taxonomy:
    category:
        - docs
---

La réflexion sur la structuration d'un SIG a comme objectif d'en permettre la bonne opérationnalité, on retrouve donc les principes de conception des systèmes d'information, avec la particularité de leur ajouter *les contraintes spécifiques des données spatiales, de leur gestion et de leur traitement*.

Ainsi, au-delà d'un logiciel dit de "Système d'Information Géographique", un SIG est, au départ, une réflexion sur l'*organisation* d'un ensemble d'activités autour de données pouvant comporter des dimensions spatiales. L'outil de SIG, comme QGIS, offre certes un groupe de fonctions qui permettent des opérations sur ces données, mais il faut d'abord concevoir le *système d'information* dans son ensemble, c'est à dire la manière dont les informations vont être acquises, stockées, gérées, interrogées, croisées, traitées, mises en forme, représentées et communiquées, diffusées.

Cela correspond donc non seulement au logiciel de SIG à proprement parler mais aussi :
* aux formats et protocoles de données à utiliser, 
* à leur organisation sous la forme de différents modes de stockage (fichiers plats de types variés, structures de données plus complexes, flux distants, capteurs...), à leur optimisation pour les requêtes (indexes, compactage...)
* aux procédures et systèmes pour gérer les entrées et sorties, éventuellement en partie automatisés avec des outils d'ETL (*extract-transform-load*) et des programmes,
* aux supports matériels, aux systèmes informatiques,
* à la maintenance et la sécurisation de ces systèmes, notamment s'ils utilisent des réseaux de données distantes (HTTPS, stockage crypté, etc.).

Dans le systèlme de SIG proprement dit, il faut notamment prendre soin :

* À **stocker** correctement l’intégralité des informations géométriques et attributaires : en préservant leur qualité (précision) et en garantissant leur préservation (redondange, sauvegardes...).

* À utiliser ** les référencements spatiaux** adaptés, qui autorisent des relations géographiques (position / distance, relations géométriques) précises.

* À gérer les **métadonnées** et préserver la connaissance sur la qualité des données (notamment pour leur mise à jour).

* À gérer **l'inter-opérabilité** et la capacité à répondre *rapidement* aux **requêtes**, dont les requêtes spatiales (formats d'échange, interfaces d'interrogration, indexes spatiaux performants...).

* À gérer les saisies et les **mises à jour** des données et faciliter **la maintenance** logicielle et matérielle du système.

Cette organisation, notamment si elle concerne un système qui doit servir plusieurs utilisateurs et durer dans le temps, donc donc être réfléchie et mise en place avec méthode.
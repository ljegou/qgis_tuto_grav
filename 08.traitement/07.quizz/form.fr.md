---
title: Quizz
taxonomy:
    category:
        - docs
form:
    name: 'Quizz traitement'
    fields:
        -
            name: name
            label: 'Nom ou pseudo'
            placeholder: 'Votre nom ou pseudo :'
            autofocus: 'on'
            autocomplete: 'on'
            type: text
            validate:
                required: true
                message: 'Saisissez votre nom ou pseudo SVP.'
        -
            name: espace1
            type: spacer
        -
            name: isochrones
            label: 'Qu''est-ce que des isochrones ?'
            type: radio
            default: null
            options:
                parcours: 'Des lignes d''égal temps de parcours'
                fuseau: 'Des lignes délimitant les fuseaux horaires'
                couleur: 'Des lignes de même couleur sur une carte'
            validate:
                required: true
                message: 'Choisissez une des propositions.'
        -
            name: espace2
            type: spacer
        -
            name: jointure
            label: 'Quelle est l''information commune (champ) qui supporte correctement les jointures attributaires ?'
            type: radio
            default: null
            options:
                nom: 'Le nom des entités'
                id: 'L''identifiant des entités'
                surface: 'La mesure de surface des entités'
            validate:
                required: true
                message: 'Choisissez un des propositions.'
        -
            name: espace3
            type: spacer
        -
            name: typecalcul
            label: 'Quel type doit-on choisir pour stocker le résultat d''un champ calculé de la part des résidences secondaires dans les logements ?'
            type: radio
            default: null
            options:
                entier: 'Nombres entiers'
                decimalzero: 'Nombres décimaux, précision zéro chiffre après la virgule'
                decimaltrois: 'Nombres décimaux, précision trois chiffres après la virgule'
            validate:
                required: true
                message: 'Choisissez une des propositions.'
        -
            name: espace4
            type: spacer
        -
            name: requete
            label: 'Quel opérateur de relations spatiales (prédicat géométrique) utiliser pour trouver les communes traversées par une rivière ?'
            type: radio
            default: null
            options:
                a: 'Rivière / croise / Commune'
                b: 'Commune / intersecte / Rivière'
                c: 'Rivière / est disjoint / Commune'
            validate:
                required: true
                message: 'Choisissez une des propositions.'
        -
            name: espace5
            type: spacer
    buttons:
        -
            type: submit
            value: Envoyer
        -
            type: reset
            value: Effacer
    process:
        -
            message: 'Vos réponses au quizz sur le traitement.'
        -
            display: trait1_quizz
---

## Le traitement : quizz